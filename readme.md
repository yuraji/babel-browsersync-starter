# Babel + BrowserSync Starter

Not too much, not too little to start a local development with ES2015

## Included

* `gulp nodemon` task, which restarts backend, when `server.js` changes.
* `gulp browsersync` task, which triggers browser to reload when any of frontend files changed.
* `gulp build` task, which builds source javascript in `src/` to `public/js/`
* `gulp watch` watches `src/` folder and calls `gulp build`
* `gulp` defaults to `gulp build`
* `npm start` is an alias to `gulp browsersync`
* Most basic `server.js` express app, which statically serves `public/` dir.
* Babel preset [es2015](https://babeljs.io/docs/plugins/preset-es2015/), with support for [es6 modules](https://hacks.mozilla.org/2015/08/es6-in-depth-modules/)

## Quick start

Install dependencies:

	npm install

Run:

	npm start
	
which will start the server with `nodemon` and `browsersync`, and serve at [localhost:3000](http://localhost:3000) (static express app), and [localhost:4000](http://localhost:4000) (includes browser-sync)

At the same time run:

	gulp watch

which will start watching javascript frontend files in `src/` and compile them to `public/js/`.


## List of included tools

* [express](http://expressjs.com/)
* [babel](https://babeljs.io/), preset [es2015](https://babeljs.io/docs/plugins/preset-es2015/)
* [browserify](http://browserify.org/), [babelify](https://github.com/babel/babelify)
* [gulp](http://gulpjs.com/), [gulp-nodemon](https://www.npmjs.com/package/gulp-nodemon), gulp-sourcemaps, gulp-uglify
* [nodemon](http://nodemon.io/)
* [browser-sync](https://www.browsersync.io/)

## How are ES6 modules compiled?

Babel only converts [ES6 modules to commonjs modules](http://babeljs.io/docs/plugins/transform-es2015-modules-commonjs/), which are not understood by browser. Browserify does the rest of the job to make the javascript browser ready.
