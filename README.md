# This fork requires babel/plugin-syntax-dynamic-import
This fork has dynamic imports activated. It requires you to install`@babel/plugin-syntax-dynamic-import`
```
npm require @babel/plugin-syntax-dynamic-import --save-dev
```

Add this to `webpack.mix.js` then continue with the default instructions below.
```
mix.babelConfig({
   plugins: ['@babel/plugin-syntax-dynamic-import'],
})
```

# Laravel Mix - Vue Auto Routing w dynamic import

This extension generate Vue Router routing automatically.

## Usage

First, install the extension.

```
npm install laravel-mix-vue-auto-routing --save-dev
npm install vue-router --save
```

Then, require it within your `webpack.mix.js` file, like so:

```js
let mix = require('laravel-mix');

require('laravel-mix-vue-auto-routing');

mix
    .js('resources/js/app.js', 'public/js')
    .vueAutoRouting();
```

```js
// /resources/js/router/index.js
import routes from 'vue-auto-routing'

import Vue from 'vue'
import Router from 'vue-router'

Vue.use(Router)

export default new Router({
    routes,
    mode: 'history',
    base: '/',
})
```

```
resources/
    js/
    └── pages/
        ├── index.vue
        ├── users.vue
        └── users/
            └── _id.vue
```
