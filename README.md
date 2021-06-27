<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->

# Basename

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] [![dependencies][dependencies-image]][dependencies-url]

> [Regular expression][regexp] to capture the last part of a Windows path.

<section class="installation">

## Installation

```bash
npm install @stdlib/regexp-basename-windows
```

</section>

<section class="usage">

## Usage

```javascript
var reBasenameWindows = require( '@stdlib/regexp-basename-windows' );
```

#### reBasenameWindows()

Returns a [regular expression][regexp] to capture the last part of a Windows path. 

```javascript
var RE = reBasenameWindows();
var base = RE.exec( 'foo\\bar\\index.js' )[ 1 ];
// returns 'index.js'
```

#### reBasenameWindows.REGEXP

[Regular expression][regexp] to capture the last part of a Windows path. 

```javascript
var match = reBasenameWindows.REGEXP.exec( 'foo\\file.pdf' )[ 1 ];
// returns 'file.pdf'
```

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
var reBasenameWindows = require( '@stdlib/regexp-basename-windows' );

var RE_BASENAME_WINDOWS = reBasenameWindows();
var base = RE_BASENAME_WINDOWS.exec( 'index.js' )[ 1 ];
// returns 'index.js'

base = RE_BASENAME_WINDOWS.exec( 'C:\\foo\\bar\\home.html' )[ 1 ];
// returns 'home.html'

base = RE_BASENAME_WINDOWS.exec( 'foo\\file.pdf' )[ 1 ];
// returns 'file.pdf'

base = RE_BASENAME_WINDOWS.exec( 'beep\\boop.' )[ 1 ];
// returns 'boop.'

base = RE_BASENAME_WINDOWS.exec( '' )[ 1 ];
// returns ''

base = RE_BASENAME_WINDOWS.exec( '\\foo\\bar\\file' )[ 1 ];
// returns 'file'

base = RE_BASENAME_WINDOWS.exec( 'C:\\foo\\bar\\.gitignore' )[ 1 ];
// returns '.gitignore'
```

</section>

<!-- /.examples -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2021. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/regexp-basename-windows.svg
[npm-url]: https://npmjs.org/package/@stdlib/regexp-basename-windows

[test-image]: https://github.com/stdlib-js/regexp-basename-windows/actions/workflows/test.yml/badge.svg
[test-url]: https://github.com/stdlib-js/regexp-basename-windows/actions/workflows/test.yml

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/regexp-basename-windows/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/regexp-basename-windows?branch=main

[dependencies-image]: https://img.shields.io/david/stdlib-js/regexp-basename-windows.svg
[dependencies-url]: https://david-dm.org/stdlib-js/regexp-basename-windows/main

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://gitter.im/stdlib-js/stdlib/

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/regexp-basename-windows/main/LICENSE

[regexp]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions

</section>

<!-- /.links -->
