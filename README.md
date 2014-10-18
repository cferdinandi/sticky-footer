# Sticky Footer [![Build Status](https://travis-ci.org/cferdinandi/sticky-footer.svg)](https://travis-ci.org/cferdinandi/sticky-footer)
Responsive sticky footers that adjust dynamically as the screen size changes.

[Download Sticky Footer](https://github.com/cferdinandi/sticky-footer/archive/master.zip) / [View the demo](http://cferdinandi.github.io/sticky-footer/)

**In This Documentation**

1. [Getting Started](#getting-started)
2. [Installing with Package Managers](#installing-with-package-managers)
3. [Working with the Source Files](#working-with-the-source-files)
4. [Options & Settings](#options-and-settings)
5. [Browser Compatibility](#browser-compatibility)
6. [How to Contribute](#how-to-contribute)
7. [License](#license)
8. [Changelog](#changelog)



## Getting Started

Compiled and production-ready code can be found in the `dist` directory. The `src` directory contains development code. Unit tests are located in the `test` directory.

### 1. Include Sticky Footer on your site.

```html
<script src="dist/js/sticky-footer.js"></script>
```

### 2. Add the markup to your HTML.

```html
<div data-sticky-wrap>
	Body content
</div>
<div data-sticky-footer>
	Footer content
</div>
```

Add the `data-sticky-wrap` attribute to a parent `<div>` that contains all of your page content. Add the `data-sticky-footer` attribute to the parent `<div>` that contains all of your footer content.

### 3. Initialize Sticky Footer.

```html
<script>
	stickyFooter.init();
</script>
```

In the footer of your page, after the content, initialize Sticky Footer. And that's it, you're done. Nice work!



## Installing with Package Managers

You can install Sticky Footer with your favorite package manager.

* **NPM:** `npm install cferdinandi/sticky-footer`
* **Bower:** `bower install https://github.com/cferdinandi/sticky-footer.git`
* **Component:** `component install cferdinandi/sticky-footer`



## Working with the Source Files

If you would prefer, you can work with the development code in the `src` directory using the included [Gulp build system](http://gulpjs.com/). This compiles, lints, and minifies code, and runs unit tests. It's the same build system that's used by [Kraken](http://cferdinandi.github.io/kraken/), so it includes some unnecessary tasks and Sass variables but can be dropped right in to the boilerplate without any configuration.

### Dependencies
Make sure these are installed first.

* [Node.js](http://nodejs.org)
* [Ruby Sass](http://sass-lang.com/install)
* [Gulp](http://gulpjs.com) `sudo npm install -g gulp`

### Quick Start

1. In bash/terminal/command line, `cd` into your project directory.
2. Run `npm install` to install required files.
3. When it's done installing, run one of the task runners to get going:
	* `gulp` manually compiles files.
	* `gulp watch` automatically compiles files when changes are made.
	* `gulp reload` automatically compiles files and applies changes using [LiveReload](http://livereload.com/).



## Options and Settings

Sticky Footer includes smart defaults and works right out of the box. But if you want to customize things, it also has a robust API that provides multiple ways for you to adjust the default options and settings.

### Global Settings

You can pass callbacks into Sticky Footer through the `init()` function:

```javascript
stickyFooter.init({
	callbackBefore: function () {}, // Runs before the footer is stuck
	callbackAfter: function () {} // Runs after the footer is stuck
});
```

### Use Sticky Footer events in your own scripts

You can also call Sticky Footer events in your own scripts.

#### destroy()
Destroy the current `stickyFooter.init()`. This is called automatically during the `init` function to remove any existing initializations.

```javascript
stickyFooter.destroy();
```



## Browser Compatibility

Sticky Footer works in all modern browsers, and IE 9 and above.

Sticky Footer is built with modern JavaScript APIs, and uses progressive enhancement. If the JavaScript file fails to load, or if your site is viewed on older and less capable browsers, footers will simply float up against the content like they normally would.



## How to Contribute

In lieu of a formal style guide, take care to maintain the existing coding style. Don't forget to update the version number, the changelog (in the `readme.md` file), and when applicable, the documentation.



## License

Sticky Footer is licensed under the [MIT License](http://gomakethings.com/mit/).



## Changelog

Sticky Footer uses [semantic versioning](http://semver.org/).

* v2.0.2 - October 18, 2014
	* Removed `.bind` dependency and polyfill.
	* Updated `gulpfile.js` tasks and namespacing.
* v2.0.1 - October 2, 2014
	* Fixed CommonJS bug.
	* Added lazypipe to `gulpfile.js`.
* v2.0.0 - August 18, 2014
	* Updated callback variables.
* v1.0.0 - August 15, 2014
	* Initial release.