# Combobox demo

[![Greenkeeper badge](https://badges.greenkeeper.io/kristianmandrup/fuse-combobox.svg)](https://greenkeeper.io/)
This [Fuse](https://www.fusetools.com/) project is configured with [Gulp](http://gulpjs.com/), [Rollup](http://rollupjs.org/) and [Babel](https://babeljs.io/) into your  workflow, allowing you to use ES2015+ features in your Fuse app.

### Demo

Based on this [fuse demo](https://www.youtube.com/watch?v=-jk3jNQzE4U) tutorial video

*Status: WIP*

## Project file structure
The project is structured as follows:

```bash
/assets
    /fonts
      - FontAwesome.otf
  /images
  /videos
- combobox.unoproj
- ComboBox.ux
- Gulpfile.js
```

## Javascript ES6

```bash
js/src
  - app.js
  - api.js
```

## Watch and rollup app.js
Run `gulp watch` to watch for changes to files in the `js/src` folder.
When a change occurs, rollup and babel will run, and your transpiled, concatenated JS file will end up as `dist/app.js`. This will in turn trigger an update in the Fuse preview simulator if it's running.

The entry point is `dist/app.js`, which means that only this file will be able to export objects to fuse.

## Watch component model files
Use `npm watch` to enable auto compilation of component model files in `/components` to `dist/components`.

## Babel support
The files in `js/src` are the source files to be used by the app. The gulp task will compile the `js/src` files to ES5 compatible javascript in `/dist` on any modification.

- `gulp` (default) - compile ES6 via Babel
- `gulp watch` - watch `js/src` for changes and compile ES6 to ES5 in `/dist`

## Create components
To create components for your app use the `component` generator.

`$ slush xfuse:component`

## Install Fuse modules

Use [fusepm](https://github.com/kristianmandrup/fusepm) to install fuse modules (libraries):

```bash
$ fusepm list
$ fusepm install <module>
```

## License

[MIT](LICENSE)
