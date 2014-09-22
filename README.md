# Node.js Version Distribution List

This is a metadata "service" written for [nvm for windows](https://github.com/coreybutler/nvm). Basically, it's a list of Node.js versions and their associated npm version, in JSON format, and automatically updated (see "How it Works"). Other version management utilities may find this useful as well.

Anyone can use the [raw data](https://raw.githubusercontent.com/coreybutler/nodedistro/master/nodeversions.json).

## How it Works

I host a script on [iron.io](http://iron.io) that runs every hour. It scrapes the [node.js release page](https://github.com/joyent/node/releases) (since the github API [returns no results](https://api.github.com/repos/joyent/node/releases)) and compares it to the current list maintained in this repository. It adds any new versions it finds to the list and commits it back to this repository.

Since the [npm-versions.txt](http://nodejs.org/dist/npm-versions.txt) is not up to date, the script depends on the release notes to determine if a new version of npm is used in the version. If no new version of npm is noted, the last known version is assumed to be used.

## Issues & Fixes

While the scraper script is fairly robust, it's still possible that erroneous data could show up. If you see an error, please submit a PR with the fix and a note about what was wrong.
