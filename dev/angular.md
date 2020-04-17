---
title: Angular KB
description: Tricks & Tips
published: true
date: 2020-04-17T15:27:49.893Z
tags: 
---

# Dependencies
- [Node.js *Node.js runtime*](/dev/nodejs)
- [VS Code *IDE*](/dev/vscode)
- [Angular CLI *Angular Command Line Interface*](https://github.com/angular/angular-cli){target='_blanck'}
{.links-list}

# Install
- Install Node js
[Download Node js](https://nodejs.org/en/download/){target='_blanck'}
- Install VS Code
[Download VS Code](https://code.visualstudio.com/){target='_blanck'}
- Install Angular CLI
[Angular Setup](https://angular.io/guide/setup-local){target='_blanck'}
`npm install -g @angular/cli`

# New Project
- Create a new project
```
ng new <project-name>
```
- Enter the folder
```
cd <project-name>
```
- First commit
```
git add .
git commit -m "init"
```
- Start Dev Server at `http://localhost:4200/`
```
ng serve --open
```
- Open in VS Code
```
code .
```

# Settings


## VS Code
- Theme: Cobalt2
- TSLint
- Editor: Format On Save = true
- Prettier: Single Quote = true

## angular.json

- set `baseHref` with the context
```json
{
  "projects": {
    "<project_name>": {
      "architect": {
        "build": {
          "configurations": {
            "production": {
              "baseHref": "/<context>/"
            }
          }
        }
      }
    }
  }
}

```

# Commands

## Angular Commands
- Start dev server
```
ng serve
```
- Generate a new component, without `.spec` file
```
ng g c --skipTests components/<name>
```