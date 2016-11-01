# Slendr [![slendr](https://img.shields.io/npm/v/slendr.svg?maxAge=2592000)](https://www.npmjs.com/package/slendr) [![Build Status](https://travis-ci.org/joseluisq/slendr.svg?branch=master)](https://travis-ci.org/joseluisq/slendr) [![JavaScript Style Guide](https://img.shields.io/badge/code%20style-standard-brightgreen.svg)](http://standardjs.com/)

> Lightweight and responsive slider for modern browsers.

Built on the top of [ES6](https://babeljs.io/docs/learn-es2015/) with minimum Javascript and [CSS3 Hardware Acceleration](http://www.html5rocks.com/en/tutorials/speed/high-performance-animations/) performance in mind.

## Install

```sh
npm install slendr --save-dev
```

## Usage

Base styles:

```html
<link rel="stylesheet" href="dist/slendr.min.css">
```

_You can customize your slider editing the `slendr.scss` file._

Markup:

```html
<div class="slendr">
  <nav class="slendr-direction">
    <a href="#" class="slendr-prev"><i class="fa fa-angle-left"></i></a>
    <a href="#" class="slendr-next"><i class="fa fa-angle-right"></i></a>
  </nav>

  <nav class="slendr-control"></nav>

  <div class="slendr-slides">
    <section class="slendr-slide" data-src="slide1.jpg"></section>
    <section class="slendr-slide" data-src="slide2.jpg"></section>
    <section class="slendr-slide" data-src="slide3.jpg"></section>
  </div>
</div>
```

API:

```js
const Slendr = require('slendr')

const slider = Slendr({
  slideshow: true
})
```

For more detailed example check out `/examples` dir.

[![view on requirebin](http://requirebin.com/badge.png)](http://requirebin.com/?gist=9baa0cf1691654c193062f7fab796f91)

## Options

```js
{
  container: '.slendr',
  selector: '.slendr-slides > .slendr-slide',
  animationClass: '.slendr-animate',
  directionNavPrev: '.slendr-prev',
  directionNavNext: '.slendr-next',
  slideActive: '.slendr-active',
  slideShowClass: '.slendr-show',
  animationSpeed: 900,
  slideshow: true,
  slideshowSpeed: 4000,
  directionNavs: true,
  keyboard: false,
  controlNavs: true,
  controlNavClass: '.slendr-control',
  controlNavClassActive: '.slendr-control-active'
}
```

## Methods

#### prev()
Move to previous slide.

```js
slendr.prev()
```

#### next()
Move to next slide.

```js
slendr.next()
```

#### move(index)
Move slider by index.

```js
slendr.move(2)
```

## Events

#### move
Trigger when slider moves to previous or next slide.

```js
slendr.on('move', (direction, index, element) => {
})
```


#### prev
Trigger when slider moves to previous slide.

```js
slendr.on('prev', (index, element) => {
})
```

#### next
Trigger when slider moves to next slide.

```js
slendr.on('next', (index, element) => {
})
```

## Contributions

[Pull requests](https://github.com/joseluisq/slendr/pulls) and [issues](https://github.com/joseluisq/slendr/issues) are welcome.

#### Development
If you can to contribute or simply play with the source try:

Install packages

```sh
$ npm install
```

Run development server

```sh
$ npm start
```

Or build dist files

```sh
$ npm run build
```

For more details, check out `scripts` in `packages.json`.

## License
MIT license

© 2016 [José Luis Quintana](http://git.io/joseluisq)
