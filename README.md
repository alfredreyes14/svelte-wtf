# create-svelte

Everything you need to build a Svelte project, powered by [`create-svelte`](https://github.com/sveltejs/kit/tree/master/packages/create-svelte).

## Creating a project

If you're seeing this, you've probably already done this step. Congrats!

```bash
# create a new project in the current directory
npm create svelte@latest

# create a new project in my-app
npm create svelte@latest my-app
```

## Developing

Once you've created a project and installed dependencies with `npm install` (or `pnpm install` or `yarn`), start a development server:

```bash
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

## Building

To create a production version of your app:

```bash
npm run build
```

You can preview the production build with `npm run preview`.

> To deploy your app, you may need to install an [adapter](https://kit.svelte.dev/docs/adapters) for your target environment.

## Prismic

For demo purposes, this project is integrated with Prismic. Check their documentation here (https://prismic.io/).

###### Important files to take note for Prismic integration
1. /lib/prismic.io.js
2. /slices/*
3. +page.js or +page.server.js

###### Notes
I highly suggest creating your own Prismic repository, to connect your newly created repo to this project follow these steps
1. Go to **/lib/prismic.io.js** and change the **line 3** with your repo name. Then change **line 8** and add your routes. If you will use slices, make sure that the uid of the document matches the **uid** in the routes object.
