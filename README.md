# Sticky Footer [![Build Status](https://travis-ci.org/cferdinandi/sticky-footer.svg)](https://travis-ci.org/cferdinandi/sticky-footer)
Responsive sticky footers that adjust dynamically as the screen size changes.

[Download Sticky Footer](https://github.com/cferdinandi/sticky-footer/archive/master.zip) / [View the demo](http://cferdinandi.github.io/sticky-footer/)

**In This Documentation**

1. [Getting Started](#getting-started)
2. [Installing with Package Managers](#installing-with-package-managers)
3. [Options & Settings](#options-and-settings)
4. [Browser Compatibility](#browser-compatibility)
5. [How to Contribute](#how-to-contribute)
6. [License](#license)
7. [Changelog](#changelog)



## Getting Started

Compiled and production-ready code can be found in the `dist` directory. The `src` directory contains development code. Unit tests are located in the `test` directory.

### 1. Include Sticky Footer on your site.

```html
<script src="dist/js/bind-polyfill.js"></script>
<script src="dist/js/sticky-footer.js"></script>
```

Sticky Footer requires `bind-polyfill.js`, a polyfill that extends ECMAScript 5 API support to more browsers.

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
Destroy the current `stickyFooter.init()`.

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

* v2.0.0 - August 18, 2014
	* Updated callback variables.
* v1.0.0 - August 15, 2014
	* Initial release.