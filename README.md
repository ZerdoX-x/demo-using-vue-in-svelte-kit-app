# What is this?

In this demo I've tried to inject simple vue component into svelte application. It turned out to be much easier than I thought and now I even doubt the existence of this repository.

## Why?

Currenty I am working on some bigger project that is currently migrating from vue to svelte. Time has come and project got too many svelte chunks made using [this fancy tool](https://github.com/pngwn/svelte-adapter) so now project needs svelte as base platform as it will be easier to mantain smaller amount of left vue chunks.

## How do I run demo?

```
git clone https://github.com/ZerdoX-x/demo-using-vue-in-svelte-kit-app.git
cd demo-using-vue-in-svelte-kit-app
npm install --global @vue/cli-service-global
npm install
npm run vue-external-components:button
npm run build
npm run preview
```

## Some explanation what's going on

1. Add vue to your application. For example using [unpkg.com](https://unpkg.com/).
2. Compile your vue component file using [vue cli](https://cli.vuejs.org/). You will need to include UMD version of compiled script to your page. Also include css file if needed.
3. Mount vue "app" with all your components included after svelte app is mounted. In this demo `sveltekit:start` event is used -- [kit.svelte.dev/docs#events](https://kit.svelte.dev/docs#events). Also please use proper mount points for both svelte and vue.

## SSR?

In this demo vue components are rendered only after svelte app is mounted. I don't know, you can give it a try and configure Vue SSR on Svelte app but I don't think it's possible or worth it.

## Any other question about this demo?

This repo is probably archivated now so you can DM me any way you like.
