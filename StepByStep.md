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



