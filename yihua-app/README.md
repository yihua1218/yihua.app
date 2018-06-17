# yihua-app

> Yi-Hua's App for personal life.

## Build Setup

``` bash
# install dependencies
$ npm install # Or yarn install

# serve with hot reload at localhost:3000
# service worker is disabled in dev
$ npm run dev

# build for production and launch server
$ npm run build
$ npm start

# generate static project
$ npm run generate
```

For detailed explanation on how things work, checkout the [Nuxt.js docs](https://github.com/nuxt/nuxt.js).

## Bootstrap

``` bash
$ yarn add bootstrap-vue
```

## Pre-processors

``` bash
$ yarn add pug pug-loader coffeescript coffee-loader node-sass sass-loader
```

## Install nuxt-fontawesome

``` bash
$ yarn add nuxt-fontawesome
$ yarn add @fortawesome/fontawesome-free-solid
```

## Social Buttons for Bootstrap

[Social Buttons for Bootstrap](https://lipis.github.io/bootstrap-social/)

``` bash
$ yarn add bootstrap-social
```

## Deploy

``` bash
$ cd dist
$ aws s3 sync --profile yihua --acl public-read --exclude .DS_Store . s3://yihua.app
```

## Reference

1. [Authentication module for Nuxt.js](https://github.com/nuxt-community/auth-module)
2. [nuxt-passport-facebook-authentication](https://github.com/tomgreener/nuxt-passport-facebook-authentication)
3. [bootstrap-vue](https://bootstrap-vue.js.org/docs/)