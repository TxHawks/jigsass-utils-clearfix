# JigSass Utils Clearfix
[![NPM version][npm-image]][npm-url]  [![Dependency Status][daviddm-image]][daviddm-url]   

 > Micro-clearfix utility class

Force an element to clear its floated child element and prevent its layout from collapsing. 

## Installation

Using npm:

```sh
npm i -S jigsass-utils-clearfix
```

## Usage
Import JigSass Utils Clearfix into your main scss file near its very end, together with all
other utilities (utilities should always be the last to be imported).

```scss
@import 'path/to/jigsass-utils-clearfix/scss/index';
```

Importing the file will create any styles by itself. You would need to indicate that the 
`.u-cf` class should actually be generated in each component or object it is used in:

```scss
// _c.foo.scss
.foo {
  @include jigsass-util(u-cf);

  ...
}
```

```scss
// _c.bar.scss
.bar {
  @include jigsass-util(u-clearfix);

  ...
}
```

```scss
// _c.baz.scss
.baz {
  @include jigsass-util(u-clearfix);

  ...
}
```

Doing so helps us a great deal with portability, as no matter where we import component or object 
partials, the correct utility classes will be generated. Think of it as a poor man's dependency
management.

Developer communication is also assisted by including "dependencies" wherever they are required,
as anyone going through a partial, can easily understand how it should be marked up with just a
glance.

As far as bloat goes, just don't worry about it - the actual styles will only be generated once, 
at the location in the cascade where the Jigsass Clearfix partial was imported into the main file.

**License:** MIT



[npm-image]: https://badge.fury.io/js/jigsass-utils-clearfix.svg
[npm-url]: https://npmjs.org/package/jigsass-utils-clearfix

[daviddm-image]: https://david-dm.org/TxHawks/jigsass-utils-clearfix.svg?theme=shields.io
[daviddm-url]: https://david-dm.org/TxHawks/jigsass-utils-clearfix
