# Gulp + Shopify

Version: 2.0.3

## Author

Jase Warner ( [https://jase.io](https://jase.io "Jase Warner’s website") )

> If this project has been a helping hand to you, feel free to [give this grateful developer a coffee](https://www.buymeacoffee.com/jasewarner/) ☕️

## Synopsis

**Update:** 2021/09/15 – This project has been updated to support Shopify CLI and [Online Store 2.0](https://www.shopify.com/partners/blog/shopify-online-store "Online Store 2.0 article") features.

*Gulp + Shopify* is for Developers wishing to use [Gulp.js](http://gulpjs.com/ "Gulp.js website") in combination with [Shopify CLI](https://shopify.dev/themes/tools/cli "Shopify CLI page") to develop Shopify themes &ndash; a tidy solution to the problem with Shopify not allowing sub-directories within the `assets` directory.

The theme is packaged with Gulp for watching and compiling assets in the `dev` directory, including SCSS, JS, images, and fonts. When modified, said assets are moved across to the `assets` directory.

A selection of helpful mixins is also included, most of which are featured in [this useful article](http://zerosixthree.se/8-sass-mixins-you-must-have-in-your-toolbox/ "Mixins article") by [@seb_ekstrom](https://twitter.com/seb_ekstrom "@seb_ekstrom on Twitter").

You may also write your JavaScript in ES6 &ndash; The Gulp scripts task uses [Babel](https://babeljs.io/ "Babel website"), so you can use the latest syntax without worrying about browser support.

The theme Liquid and JSON files are all blank canvases – zero faffing, meaning you can crack on with the build right away.

The theme includes the Bootstrap 5 grid and reboot scss files. These can be removed in `theme.scss.liquid` and `password.scss.liquid`, or, if you so wish, you may add more Bootstrap SCSS files using @import via `./node_modules/bootstrap/scss/`.

## Installation

### Gulp.js

Clone the repo into your project root.

In Terminal `cd` into the `dev` directory and install the Gulp packages (if you haven’t already installed Gulp, you’ll need to [do so](https://github.com/gulpjs/gulp/blob/master/docs/getting-started.md "Gulp installation") first):

`npm install`

Once you have installed the packages, in Terminal, run `gulp` and then `gulp watch`.

Any changes to the SCSS files in `dev/sass/` will be reflected in `theme.css.liquid` and/or `password.css.liquid` in `assets`.

Any alterations to the JS files in `dev/js/` will be concatenated and uglified in `assets` to `theme.js`.

Images added to `dev/image` will be copied across to the `assets` directory. Similarly, any fonts added to `dev/font` will be copied across to `assets`.

### Shopify CLI

To get Shopify CLI up and running, follow the instructions [here](https://shopify.dev/themes/tools/cli/installation "Shopify CLI installation instructions").

To get started on your theme, follow [these instructions](https://shopify.dev/themes/tools/cli/getting-started "Shopify CLI usage instructions").

> Important: Unfortunately the Shopify CLI hot reload feature fires too soon for Shopify to serve any updated assets, such as CSS or JS. I’ve only been working with Shopify CLI for a couple of weeks now, so maybe I’ve missed something, but I’m finding that a manual reload (delayed by a second or two) is still required after every change.

## Features

The Gulp build features the following helpful packages:

* [gulp-autoprefixer](https://github.com/sindresorhus/gulp-autoprefixer "gulp-autoprefixer GitHub page")
* [gulp-babel](https://github.com/babel/gulp-babel "gulp-babel GitHub page")
* [gulp-concat](https://github.com/contra/gulp-concat "gulp-concat GitHub page")
* [gulp-rename](https://github.com/hparra/gulp-rename "gulp-rename GitHub page")
* [gulp-replace](https://github.com/lazd/gulp-replace "gulp-replace GitHub page")
* [gulp-sass](https://github.com/dlmanning/gulp-sass "gulp-sass GitHub page")
* [gulp-uglify](https://github.com/terinjokes/gulp-uglify "gulp-uglify GitHub page")
* [gulp-scss-lint](https://github.com/juanfran/gulp-scss-lint "gulp-scss-lint GitHub page")

## Credits

* [Gulp.js](http://gulpjs.com/ "Gulp.js website")
* [Shopify CLI](https://shopify.dev/themes/tools/cli "Shopify CLI page")
* [SASS / SCSS](http://sass-lang.com/ "SASS website")
