# PWA Starter App
Use this template to start building your app.

## How to use it?
### Two main-options with sub-options

| There are two main-options in GitHub: | ![](https://raw.githubusercontent.com/lovkyndig/pwa-starter-app/main/public/img/webp/two-buttons.webp) |

The buttons have two/ three sub-options:

| `<> Code`-btn | `Use this template`-btn |
| --- | --- |
| Download it | Create a new repository | 
| Open in GitHub Desktop | Open in codespace | 
| Create CodeSpace on Main |  | 

The best choice is `Codespace`.

### Install
This step is necessary if you don't select `Codespace`.

If you already are a developer you know that you have to install the dependencies[^1] in the `packages.json`-file like this:
```bash
npm install
```
And then you know how to change `npm` with `yarn`, `npmn` etc.

## The node-scripts
If you open up the `package.json`-file you will see all the script-options:  
```json
"scripts": {
  "dev": "nuxt dev",
  "build": "nuxt build",
  "generate": "nuxt generate && npx pagefind --source dist",
  "preview": "nuxt preview"
},
```

If you don't want to use `yarn preview` options you have after running `yarn build` or `yarn generate`, you can type `yarn dev`, and open your browser on `localhost:3000`, to see how the website is looking like.[`2]

### Pagefind
If you don't want to add `_pagefind` to the `public`-folder every time you type `npm generate`, you can just change the **generate**-line and add a new `bach-/ batch`-command:
```bash
"generate": "nuxt generate",
"pagefind": "npx pagefind --source dist"
```

Then on the end when you are finish testing your repo with `dev / build / generate /preview`, you can just run:
```bash
npm pagefind
```

Now the user has the possibility to search trough all your articles, and find word or strings.

## Content
All the articles has to be written in `md`-format and placed in the `content`-folder.

### MDC
There are some `MD`-components that can be used. If someone else than me is using this template, send me a message or question, then I tell you about it.

Or you can look inside `node_modules/@lovkyndig/create-google-app/components/content/`-folder. You find all the `mdc`.

_Updated 22.11.2023_

[^]: In this repo there are only one dependency: `@lovkyndig/create-google-app`. Of cause you need [Node.js](https://nodejs.org/) on your PC. And if you don't want to use `npm` you can add another package managers like [yarn](https://yarnpkg.com/) globally in your local PC.
[^2]: If you don't have installed `yarn` in your local mashine, write: `npm help` to see how to use `npm`. `npm run dev` is the alternative to `yarn dev`.