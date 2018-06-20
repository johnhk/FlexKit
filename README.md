# FlexKit Starter

# FlexKit

Starter Kit for Angular 6 + WebPack 4

## Development server

Run `npm run-script start` for a dev server. Navigate to `http://localhost:9090/`. The app will automatically reload if you change any of the source files.

## Build

Run `npm run-script build` to build the project. The build artifacts will be stored in the `dist/` directory. 

## Production

Run `npm run-script prod` to generate a production build of the project. The build artifacts will be stored in the `dist/` directory. 


## Features

- Webpack v4.8.3 
- Angular v6.0.5
- Typescript v2.8.3

## Folder and Files

We use the component approach in our starter. This is the new standard for developing Angular apps and a great way to ensure maintainable code by encapsulation of our behavior logic. A component is basically a self contained app usually in a single file or a folder with each concern as a file: style, template, specs, e2e, and component class. Here's how it looks:

````    
angular-starter/
 ├──config/                        * our configuration
 │   │                              
 |   ├──helpers.js                 * helper functions for our configuration files
 │   ├──webpack.common.js          * common tasks for webpack build process shared for dev and prod
 │   ├──webpack.dev.js             * our development webpack config
 │   └──webpack.prod.js            * our production webpack config
 │
 ├──src/                           * our source files that will be compiled to javascript
 │   ├──main.ts                    * our entry file for our browser environment
 │   ├──index.html                 * Index.html: where we generate our index page
 │   ├──tsconfig.json              * typescript config used outside webpack
 │   ├──tslint.json                * typescript lint config
 │   ├──polyfills.ts               * our polyfills file
 │   ├──vendor.ts                  * our vendor specific file
 │   │
 │   ├──app/                                    * WebApp: folder
 │   │   ├──components/
 │   │   │    └──component-example/            * Folder holding specific component called exsample
 │   │   │         ├──example.component.css    * component specific css 
 │   │   │         ├──example.component.html   * component template
 │   │   │         └──example.component.ts     * example component TypeScript file
 │   │   ├──app.component.css                   * css specific for app-component
 │   │   ├──app.component.html                  * template for app-component
 │   │   ├──app.component.ts                    * The Main app component. Container for the app
 │   │   ├──app.module.ts                       * Root module that you bootstrap to launch the applicatio
 │   │   └──appscss.component.scss              * \\ TODO
 │   │
 │   └──assets/                    * static assets are served here
 │       ├──css/
 │       │   ├──global_styles.scss * \\ TODO
 │       │   └──styles.css         * \\ TODO
 │       ├──images/
 │       │   └──angular.png        * \\ TODO
 │       ├──robots.txt             * for search engines to crawl your website
 │       └──humans.txt             * for humans to know who the developers are
 │
 │
 ├──.editorconfig                  * configuration file for EditorConfig extension
 ├──.gitignore                     * Git configuration file. Specifies intentionally untracked files to ignore
 ├──readme.md                      * Markdown file used to generate the html documnetation or summary of a projects
 ├──package.json                   * what npm uses to manage its dependencies
 ├──package.lock.json              * \\TODO what npm uses to manage its dependencies
 └──webpack.config.js              * webpack main configuration file

````

# Package.json

## Scripts

- start
- prod
- build
- clean

## dependencies
- @angular/common
  - vesion: ^6.0.5 - [Link to NPM](https://www.npmjs.com/package/@angular/common "npm")  When you want to use NgIf, NgFor
- @angular/compiler
  - vesion: ^6.0.5 - [Link to NPM](https://www.npmjs.com/package/@angular/compiler "npm") \\TODO
- @angular/core
  - vesion: ^6.0.5 - [Link to NPM](https://www.npmjs.com/package/@angular/core "npm")  Low level 'core' features in Angular such as Types, Decorators, component, Directives ...
- @angular/forms
  - vesion: ^6.0.5 - [Link to NPM](https://www.npmjs.com/package/@angular/forms "npm")  When you want to build reactive forms or When you want to build template driven forms (includes NgModel)
- @angular/http
  - vesion: ^6.0.5 - [Link to NPM](https://www.npmjs.com/package/@angular/http "npm")  When you want to talk to a server
- @angular/platform-browser
  - vesion: ^6.0.5 - [Link to NPM](https://www.npmjs.com/package/@angular/platform-browser "npm")  When you want to run your app in a browser
- @angular/platform-browser-dynamic
  - vesion: ^6.0.5 - [Link to NPM](https://www.npmjs.com/package/@angular/platform-browser-dynamic "npm")  \\TODO When you want to run your app in a browse
- @angular/router
  - vesion: ^6.0.5 - [Link to NPM](https://www.npmjs.com/package/@angular/router "npm")  When you want to use RouterLink, .forRoot(), and .forChild()
- bootstrap
  - vesion: ^4.1.1 - [Link to NPM](https://www.npmjs.com/package/bootstrap "npm")  
  Sleek, intuitive, and powerful front-end framework for faster and easier web development
- core-js
  - vesion: ^2.5.5 - [Link to NPM](https://www.npmjs.com/package/core-js "npm")  
  Modular standard library for JavaScript. Includes polyfills for ECMAScript 5, ECMAScript 6: promises, symbols, collections, iterators, typed arrays, ECMAScript 7+ proposals, setImmediate, etc. Some additional features such as dictionaries or extended partial application. You can require only needed features or use it without global namespace pollution.
- optimize-css-assets-webpack-plugin
  - vesion: ^4.0.1 - [Link to NPM](https://www.npmjs.com/package/optimize-css-assets-webpack-plugin "npm")  
  A Webpack plugin to optimize \ minimize CSS assets.  It will search for CSS assets during the Webpack build and will optimize \ minimize the CSS (by default it uses cssnano but a custom CSS processor can be specified).
- rxjs
  - vesion: ^6.1.0 - [Link to NPM](https://www.npmjs.com/package/rxjs "npm")  
  The Reactive Extensions for JavaScript (RxJS) is a set of libraries for composing asynchronous and event-based programs using observable sequences and fluent query operators that many of you already know by Array#extras in JavaScript. Using RxJS, developers represent asynchronous data streams with Observables, query asynchronous data streams using our many operators, and parameterize the concurrency in the asynchronous data streams using Schedulers. Simply put, RxJS = Observables + Operators + Schedulers.
- zone.js
  - vesion: ^0.8.26 - [Link to NPM](https://www.npmjs.com/package/zone.js "npm")  
  A Zone is an execution context that persists across async tasks. You can think of it as thread-local storage for JavaScript VMs. zone.js patches the async APIs described above, but those patches will have some overhead. Starting from zone.js v0.8.9, you can choose which web API module you want to patch

## devDependencies

- @types/node
	- ^10.0.4 - [Link to NPM](https://www.npmjs.com/package/@types/node "npm")  This package contains type definitions for Node.js
- angular2-template-loader
	- ^0.6.2 - [Link to NPM](https://www.npmjs.com/package/angular2-template-loader "npm")  Chain-to loader for webpack that inlines all html and style's in angular2 components.
- awesome-typescript-loader
	- ^5.0.0 - [Link to NPM](https://www.npmjs.com/package/awesome-typescript-loader "npm")  Awesome TypeScript loader for webpack
- cross-env
	- ^5.1.4 - [Link to NPM](https://www.npmjs.com/package/cross-env "npm")  Most Windows command prompts will choke when you set environment variables with NODE_ENV=production like that. (The exception is Bash on Windows, which uses native Bash.) Similarly, there's a difference in how windows and POSIX commands utilize environment variables. With POSIX, you use: $ENV_VAR and on windows you use %ENV_VAR%. cross-env makes it so you can have a single command without worrying about setting or using the environment variable properly for the platform. Just set it like you would if it's running on a POSIX system, and cross-env will take care of setting it properly.
- css-loader
	- ^0.28.11 - [Link to NPM](https://www.npmjs.com/package/css-loader "npm")  The css-loader interprets @import and url() like import/require() and will resolve them.
- file-loader
	- ^1.1.11 - [Link to NPM](https://www.npmjs.com/package/file-loader "npm")  Instructs webpack to emit the required object as file and to return its public URL
- html-loader
	- ^0.5.5 - [Link to NPM](https://www.npmjs.com/package/html-loader "npm")  Exports HTML as string. HTML is minimized when the compiler demands.
- html-webpack-plugin
	- ^3.2.0 - [Link to NPM](https://www.npmjs.com/package/html-webpack-plugin "npm")  Plugin that simplifies creation of HTML files to serve your bundles
- mini-css-extract-plugin
	- ^0.4.0 - [Link to NPM](https://www.npmjs.com/package/mini-css-extract-plugin "npm")  This plugin extract CSS into separate files. It creates a CSS file per JS file which contains CSS. It supports On-Demand-Loading of CSS and SourceMaps. It builds on top of a new webpack v4 feature (module types) and requires webpack 4 to work.
- node-sass
	- ^4.9.0 - [Link to NPM](https://www.npmjs.com/package/node-sass "npm")  Node-sass is a library that provides binding for Node.js to LibSass, the C version of the popular stylesheet preprocessor, Sass. It allows you to natively compile .scss files to css at incredible speed and automatically via a connect middleware.
- null-loader
	- ^0.1.1 - [Link to NPM](https://www.npmjs.com/package/null-loader "npm")  A loader that returns an empty module.
- raw-loader
	- ^0.5.1 - [Link to NPM](https://www.npmjs.com/package/raw-loader "npm")  A loader for webpack that allows importing files as a String
- rimraf
	- ^2.6.2 - [Link to NPM](https://www.npmjs.com/package/rimraf "npm")  The UNIX command rm -rf for node.
- sass-loader
	- ^7.0.1 - [Link to NPM](https://www.npmjs.com/package/sass-loader "npm")  WebPack loader. Loads a Sass/SCSS file and compiles it to CSS
- style-loader
	- ^0.21.0 - [Link to NPM](https://www.npmjs.com/package/style-loader "npm")  Adds CSS to the DOM by injecting a `<style>` tag
- to-string-loader
	- ^1.1.5 - [Link to NPM](https://www.npmjs.com/package/to-string-loader "npm")  to-string loader for webpack
- tslint
	- ^5.10.0 - [Link to NPM](https://www.npmjs.com/package/tslint "npm")  TSLint is an extensible static analysis tool that checks TypeScript code for readability, maintainability, and functionality errors. It is widely supported across modern editors & build systems and can be customized with your own lint rules, configurations, and formatters.
- tslint-config-airbnb
	- ^5.8.0 - [Link to NPM](https://www.npmjs.com/package/tslint-config-airbnb "npm")  A TSLint config for [Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript, "Airbnb JavaScript Style Guide")
- tslint-loader
	- ^3.6.0 - [Link to NPM](https://www.npmjs.com/package/tslint-loader "npm")  Tslint loader for Webpack.
- typescript
	- ^2.8.3 - [Link to NPM](https://www.npmjs.com/package/typescript "npm")  TypeScript is a language for application-scale JavaScript. TypeScript adds optional types, classes, and modules to JavaScript. TypeScript supports tools for large-scale JavaScript applications for any browser, for any host, on any OS. TypeScript compiles to readable, standards-based JavaScript.
- uglifyjs-webpack-plugin
	- ^1.2.5 - [Link to NPM](https://www.npmjs.com/package/uglifyjs-webpack-plugin "npm")  WebPack Plugin. This plugin uses UglifyJS v3 (`uglify-es`) to minify your JavaScript
- webpack
	- ^4.8.3 - [Link to NPM](https://www.npmjs.com/package/webpack "npm")  webpack is a module bundler. Its main purpose is to bundle JavaScript files for usage in a browser, yet it is also capable of transforming, bundling, or packaging just about any resource or asset.
- webpack-bundle-analyzer
	- ^2.11.1 - [Link to NPM](https://www.npmjs.com/package/webpack-bundle-analyzer "npm")  Visualize size of webpack output files with an interactive zoomable treemap.
- webpack-cli
	- ^2.0.14 - [Link to NPM](https://www.npmjs.com/package/webpack-cli "npm")  Webpack CLI encapsulates all code related to CLI handling. It captures options and sends them to webpack compiler. You can also find functionality for initializing a project and migrating between versions
- webpack-dev-server
	- ^3.1.4 - [Link to NPM](https://www.npmjs.com/package/webpack-dev-server "npm")  Use webpack with a development server that provides live reloading. This should be used for development only. It uses webpack-dev-middleware under the hood, which provides fast in-memory access to the webpack assets.
- webpack-merge
	- ^4.1.2" - [Link to NPM](https://www.npmjs.com/package/webpack-merge "npm")  webpack-merge provides a merge function that concatenates arrays and merges objects creating a new object. If functions are encountered. it will execute them, run the results through the algorithm, and then wrap the returned values within a function again. This behavior is particularly useful in configuring webpack although it has uses beyond it. Whenever you need to merge configuration objects, webpack-merge can come in handy

## MNotes
- some notes

## ToDo

- Add Testing
- Clean up and add final loaders
- Add more to production mode
- Add .... 


### Prerequisites

You will need the following to use this boilerplate

```bash

// Latest Npm
npm i -g npm@latest

// Sass
gem intall sass

// Typescript & Lint
npm i -g typescript tslint

```

## Further help

To get more help .....

@startuml

Bob -> Alice: Hello!

@enduml
