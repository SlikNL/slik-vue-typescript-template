# Slik-Vue-TypeScript-Template
A Vue / Typescript template for use with the vue-cli. Meant for internal use at Internetbureau Slik. It uses both `TypeScript` and `LESS`.

# Installation

Prerequisites: [Node.js](https://nodejs.org/en/) (>=4.x, 6.x preferred), npm version 3+ and [Git](https://git-scm.com/).

``` bash
$ npm install -g vue-cli
```

# Usage

vue init lavandongen/vue-typescript-template `<project-name>`

Example:

``` bash
$ vue init SlikNL/slik-vue-typescript-template my-project
```

The above command downloads the template and makes a new project at `./my-project/`.Then follow the insctructions in your terminal and choose whether or not you want the project to be started automatically. If you choose not to use that, or you come back to the project, you can use the following command to get started (if you have not yet installed with npm, remember to do so with `npm install`):

```
$ npm run dev
```

Setup may take a few minutes.. Get a drink.

# In Addition

## vue router

add the `vue router` option at initialization time, it will set up the project to use vue router. It will configure in the `src/router` folder, like this:

```
src
├──router
   ├──index.ts
```

## vuex
add the `vuex` option at initialization time, it will create `src/store` folder, and be configured, like this:

```
src
├──store
   ├──actions.ts
   ├──mutations.ts
   ├──getters.ts
   ├──types.ts
```

## vue-property-decorator
`vue-property-decorator` is added by default. It will make it much easier to refracture the code and also easier to add properties like watch to the component classes.

# What's Included

- `npm run dev`: first-in-class development experience.
  - Webpack + `vue-loader` for single file Vue components.
  - State preserving hot-reload
  - State preserving compilation error overlay
  - Lint-on-save with ESLint (when enabled)
  - Source maps

- `npm run build`: Production ready build.
  - JavaScript minified with [UglifyJS v3](https://github.com/mishoo/UglifyJS2/tree/harmony).
  - HTML minified with [html-minifier](https://github.com/kangax/html-minifier).
  - CSS across all components extracted into a single file and minified with [cssnano](https://github.com/ben-eb/cssnano).
  - Static assets compiled with version hashes for efficient long-term caching, and an auto-generated production `index.html` with proper URLs to these generated assets.
  - Use `npm run build --report` to build with bundle size analytics.

- `npm run unit`: Unit tests run in [JSDOM](https://github.com/tmpvar/jsdom) with [Jest](https://facebook.github.io/jest/), or in PhantomJS with Karma + Mocha + karma-webpack.
  - Supports ES2015+ in test files.
  - Easy mocking.

- `npm run e2e`: End-to-end tests with [Nightwatch](http://nightwatchjs.org/).
  - Run tests in multiple browsers in parallel.
  - Works with one command out of the box:
    - Selenium and chromedriver dependencies automatically handled.
    - Automatically spawns the Selenium server.

&nbsp;

#### Disclaimer

> this template was initially forked from [SimonZhangITer/vue-typescript-template](https://github.com/SimonZhangITer/vue-typescript-template) and was changed for internal use at Internetbureau Slik by [Lucas van Dongen](https://github.com/lavandongen). It should not be used for projects outside of Internetbureau Slik. If you encounter any issue with the use of this template you can reach Lucas at lucas@slik.eu or lucasvandongen10@gmail.com (or go to town and try to fix it yourself)
