title: Build Commands
---
We will be covering Development and Production build commands. For a full list of Quasar CLI commands, make sure to read its [documentation page](/guide/quasar-cli.html).

### Development
> Starts a Node.js local development server.

``` bash
# run development server (with default theme)
$ quasar dev

# run development server with specific theme
$ quasar dev -t mat
$ quasar dev -t ios

# on specific port
$ quasar dev -p 9090

# PWA
$ quasar dev -m pwa

# Mobile App
$ quasar dev -m cordova -T [android|ios] -t [mat|ios]

# Electron App
$ quasar dev -m electron
# with iOS theme...
$ quasar dev -m electron -t ios
```

For a complete list, please read [Quasar CLI](/guide/quasar-cli.html#dev-Development-Server) Development Server section.

While developing with the Dev Server you will have:
* Babel, so you can write ES6 code
* Webpack + vue-loader for Vue SFC (single file components)
* State preserving hot-reload
* State preserving compilation error overlay
* Lint-on-save with ESLint
* Source maps
* Develop right on a device emulator (or a real phone connected to your machine) if you target a Mobile App
* Develop right on an Electron window with Developer Tools included if you target an Electron App

### Production
> Build assets for production.

``` bash
# build for production
$ quasar build

# build for production with specific theme
$ quasar build -t mat
$ quasar build -t ios

# PWA
$ quasar build -m pwa

# Mobile App
$ quasar build -m cordova -T [android|ios] -t [mat|ios]

# Electron App
$ quasar build -m electron
# with iOS theme...
$ quasar build -m electron -t ios
```

For a complete list, please read [Quasar CLI](/guide/quasar-cli.html#build-clean-Build-App-for-Production) Build App for Production section.

In addition to what you get while developing your website/app, for production builds you also take advantage of:
* Javascript minified with [UglifyJS](https://github.com/mishoo/UglifyJS2)
* HTML minified with [html-minifier](https://github.com/kangax/html-minifier)
* CSS across all components extracted (and auto-prefixed) into a single file and minified with [cssnano](https://github.com/ben-eb/cssnano)
* All static assets are compiled with version hashes for efficient long-term caching, and a production index.html is auto-generated with proper URLs to these generated assets.
