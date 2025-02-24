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


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# reBasenameWindows

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> [Regular expression][regexp] to capture the last part of a Windows path.



<section class="usage">

## Usage

```javascript
import reBasenameWindows from 'https://cdn.jsdelivr.net/gh/stdlib-js/regexp-basename-windows@esm/index.mjs';
```

You can also import the following named exports from the package:

```javascript
import { REGEXP } from 'https://cdn.jsdelivr.net/gh/stdlib-js/regexp-basename-windows@esm/index.mjs';
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

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="module">

import reBasenameWindows from 'https://cdn.jsdelivr.net/gh/stdlib-js/regexp-basename-windows@esm/index.mjs';

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

</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

* * *

## See Also

-   <span class="package-name">[`@stdlib/regexp-basename`][@stdlib/regexp/basename]</span><span class="delimiter">: </span><span class="description">return a regular expression to capture the last part of a path.</span>
-   <span class="package-name">[`@stdlib/regexp-basename-posix`][@stdlib/regexp/basename-posix]</span><span class="delimiter">: </span><span class="description">return a regular expression to capture the last part of a POSIX path.</span>

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2025. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/regexp-basename-windows.svg
[npm-url]: https://npmjs.org/package/@stdlib/regexp-basename-windows

[test-image]: https://github.com/stdlib-js/regexp-basename-windows/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/regexp-basename-windows/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/regexp-basename-windows/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/regexp-basename-windows?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/regexp-basename-windows.svg
[dependencies-url]: https://david-dm.org/stdlib-js/regexp-basename-windows/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/regexp-basename-windows/tree/deno
[deno-readme]: https://github.com/stdlib-js/regexp-basename-windows/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/regexp-basename-windows/tree/umd
[umd-readme]: https://github.com/stdlib-js/regexp-basename-windows/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/regexp-basename-windows/tree/esm
[esm-readme]: https://github.com/stdlib-js/regexp-basename-windows/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/regexp-basename-windows/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/regexp-basename-windows/main/LICENSE

[regexp]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions

<!-- <related-links> -->

[@stdlib/regexp/basename]: https://github.com/stdlib-js/regexp-basename/tree/esm

[@stdlib/regexp/basename-posix]: https://github.com/stdlib-js/regexp-basename-posix/tree/esm

<!-- </related-links> -->

</section>

<!-- /.links -->
