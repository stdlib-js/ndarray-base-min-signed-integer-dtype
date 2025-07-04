<!--

@license Apache-2.0

Copyright (c) 2024 The Stdlib Authors.

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

# Minimum Data Type

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Determine the minimum ndarray [data type][@stdlib/ndarray/dtypes] for storing a provided signed integer value.

<!-- Section to include introductory text. Make sure to keep an empty line after the intro `section` element and another before the `/section` close. -->

<section class="intro">

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->

<section class="installation">

## Installation

```bash
npm install @stdlib/ndarray-base-min-signed-integer-dtype
```

Alternatively,

-   To load the package in a website via a `script` tag without installation and bundlers, use the [ES Module][es-module] available on the [`esm`][esm-url] branch (see [README][esm-readme]).
-   If you are using Deno, visit the [`deno`][deno-url] branch (see [README][deno-readme] for usage intructions).
-   For use in Observable, or in browser/node environments, use the [Universal Module Definition (UMD)][umd] build available on the [`umd`][umd-url] branch (see [README][umd-readme]).

The [branches.md][branches-url] file summarizes the available branches and displays a diagram illustrating their relationships.

To view installation and usage instructions specific to each branch build, be sure to explicitly navigate to the respective README files on each branch, as linked to above.

</section>

<section class="usage">

## Usage

```javascript
var minSignedIntegerDataType = require( '@stdlib/ndarray-base-min-signed-integer-dtype' );
```

#### minSignedIntegerDataType( value )

Returns the minimum ndarray [data type][@stdlib/ndarray/dtypes] for storing a provided signed integer value.

```javascript
var dt = minSignedIntegerDataType( 9999 );
// returns 'int16'

dt = minSignedIntegerDataType( -3 );
// returns 'int8'

dt = minSignedIntegerDataType( 3 );
// returns 'int8'

dt = minSignedIntegerDataType( 1e100 );
// returns 'float64'
```

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

## Notes

-   Once a provided integer value exceeds the maximum values of all supported signed integer [data types][@stdlib/ndarray/dtypes], the function defaults to returning `'float64'`.

</section>

<!-- /.notes -->

<!-- Package usage examples. -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
var discreteUniform = require( '@stdlib/random-array-discrete-uniform' );
var exp2 = require( '@stdlib/math-base-special-exp2' );
var minSignedIntegerDataType = require( '@stdlib/ndarray-base-min-signed-integer-dtype' );

// Generate random powers:
var exp = discreteUniform( 100, 0, 40, {
    'dtype': 'generic'
});

// Determine the minimum data type for each generated value...
var v;
var i;
for ( i = 0; i < exp.length; i++ ) {
    v = exp2( exp[ i ] );
    console.log( 'min(%d) => %s', v, minSignedIntegerDataType( v ) );
}
```

</section>

<!-- /.examples -->

<!-- Section to include cited references. If references are included, add a horizontal rule *before* the section. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="references">

</section>

<!-- /.references -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


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

Copyright &copy; 2016-2025. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/ndarray-base-min-signed-integer-dtype.svg
[npm-url]: https://npmjs.org/package/@stdlib/ndarray-base-min-signed-integer-dtype

[test-image]: https://github.com/stdlib-js/ndarray-base-min-signed-integer-dtype/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/ndarray-base-min-signed-integer-dtype/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/ndarray-base-min-signed-integer-dtype/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/ndarray-base-min-signed-integer-dtype?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/ndarray-base-min-signed-integer-dtype.svg
[dependencies-url]: https://david-dm.org/stdlib-js/ndarray-base-min-signed-integer-dtype/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/ndarray-base-min-signed-integer-dtype/tree/deno
[deno-readme]: https://github.com/stdlib-js/ndarray-base-min-signed-integer-dtype/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/ndarray-base-min-signed-integer-dtype/tree/umd
[umd-readme]: https://github.com/stdlib-js/ndarray-base-min-signed-integer-dtype/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/ndarray-base-min-signed-integer-dtype/tree/esm
[esm-readme]: https://github.com/stdlib-js/ndarray-base-min-signed-integer-dtype/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/ndarray-base-min-signed-integer-dtype/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/ndarray-base-min-signed-integer-dtype/main/LICENSE

[@stdlib/ndarray/dtypes]: https://github.com/stdlib-js/ndarray-dtypes

</section>

<!-- /.links -->
