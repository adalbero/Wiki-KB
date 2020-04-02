---
title: Node.js
description: 
published: true
date: 2020-04-02T18:11:37.568Z
tags: 
---


# Node.js
![Image](https://upload.wikimedia.org/wikipedia/commons/d/d9/Node.js_logo.svg =x50)

You can install **node.js** by downloading the latest version from https://nodejs.org, or use [Node Version Manager](#node-version-manager).

### Links
- [https://nodejs.org *Node.js Home Page*](https://nodejs.org)
{.links-list}



# Node Version Manager (nvm)

- `nvm list available` : list all available node versions to download
- `nvm list` : list all installed node versions
- `nvm install <version>` : install specific version of node.js
- `nvm install latest` : install latest stable version
- `nvm uninstall <version>` : uninstall specific version of node.js
- `nvm root` : show the path where node will be installed
- `nvm use <version>` : switch to an installed version of node.js
{.grid-list}

### Tips
> Note that any global modules installed in one version will not be shared with other versions.
{.is-warning}

### Links
- [https://github.com/nvm-sh/nvm *nvm Linux/Mac Version*](https://github.com/nvm-sh/nvm)
- [https://github.com/coreybutler/nvm-windows *nvm Windows Version*](https://github.com/coreybutler/nvm-windows)
{.links-list}

# Node Package Manager (npm)

`npm` is installed automatically with `node.js`

- 'npm init -y' : create a new node project in the current folder
- `npm install <module>` : install `module` locally
- `npm install -g <module>` : install `module` globally
- `npm list -g -depth 0` : list all installed modules globally
{.grid-list}



