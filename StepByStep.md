## Install the development environment

### Use nvm to manage node.js versions

- https://github.com/creationix/nvm#installation
- https://github.com/creationix/nvm#usage

### Install node

```
$ echo "lts/*" > .nvmrc # to default to the latest LTS version
$ nvm use
Found '/private/var/www/study/vw-layout-in-vue/.nvmrc' with version <lts/*>
Now using node v10.15.0 (npm v6.5.0)
```

### Install Vue-cli

```
$ npm install -g @vue/cli
$ vue --version
3.2.3
```

## Use Vue-cli to create a project

### Creating a Project

```
$ vue create vw-layout-in-vue
? Please pick a preset: Manually select features
? Check the features needed for your project: Babel, Router, Vuex, CSS Pre-processors, Linter, Unit
? Use history mode for router? (Requires proper server setup for index fallback in production) Yes
? Pick a CSS pre-processor (PostCSS, Autoprefixer and CSS Modules are supported by default): Sass/SCSS
? Pick a linter / formatter config: Standard
? Pick additional lint features: (Press <space> to select, <a> to toggle all, <i> to invert selection)Lint on save
? Pick a unit testing solution: Mocha
? Where do you prefer placing config for Babel, PostCSS, ESLint, etc.? In dedicated config files

🎉  Successfully created project vm-layout-in-vue.
👉  Get started with the following commands:

 $ cd vm-layout-in-vue
 $ npm run serve
```

### Using the GUI

```
$ vue ui
```

### Install PostCSS plugins

```
$ npm i postcss-import postcss-url postcss-preset-env cssnano cssnano-preset-advanced postcss-px-to-viewport postcss-aspect-ratio-mini postcss-write-svg --save-dev
```

Next, configure the newly installed PostCSS plugins in the.postcssrc.js file.

```
module.exports = {
  plugins: {
    'postcss-import': {},
    'postcss-url': {},
    'postcss-aspect-ratio-mini': {},
    'postcss-write-svg': { utf8: false },
    'postcss-preset-env': {},
    'postcss-px-to-viewport': {
      viewportWidth: 750, // (Number) The width of the viewport.
      viewportHeight: 1334, // (Number) The height of the viewport.
      unitPrecision: 3, // (Number) The decimal numbers to allow the REM units to grow to.
      viewportUnit: 'vw', // (String) Expected units.
      selectorBlackList: ['.ignore', '.hairlines'], // (Array) The selectors to ignore and leave as px.
      minPixelValue: 1, // (Number) Set the minimum pixel value to replace.
      mediaQuery: false // (Boolean) Allow px to be converted in media queries.
    },
    'cssnano': {
      preset: 'advanced',
      autoprefixer: false,
      'postcss-zindex': false
    }
  }
}
```

### Add px to vw, 1px background line and aspect-ratio demos

Please see the About page.