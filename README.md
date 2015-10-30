**UPDATE: 10/30/2015**

The script has been rewritten to support the new release process (i.e. supporting Node v4.0.0+).

# Node.js Version Distribution List

This is a metadata "service" written for [nvm for windows](https://github.com/coreybutler/nvm). Basically, it's a list of Node.js versions and their associated npm version, in JSON format, and automatically updated (see "How it Works"). Other version management utilities may find this useful as well.

Anyone can use the [raw data](https://raw.githubusercontent.com/coreybutler/nodedistro/master/nodeversions.json).

## How it Works

I host a script on [iron.io](http://iron.io) that runs every hour. It scrapes the [node.js releases](http://nodejs.org/dist/index.json) and compares it to the current list maintained in this repository. It adds any new versions it finds to the list and commits it back to this repository.

## Issues & Fixes

While the scraper script is fairly robust, it's still possible that erroneous data could show up in the data here. If you see an error in the data here, please submit a PR with the fix and a note about what was wrong. The script won't overwrite manual changes.
