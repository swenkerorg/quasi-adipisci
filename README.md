# String.prototype.trim <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![dependency status][deps-svg]][deps-url]
[![dev dependency status][dev-deps-svg]][dev-deps-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

An ES5 spec-compliant `String.prototype.trim` shim. Invoke its "shim" method to shim `String.prototype.trim` if it is unavailable.

This package implements the [es-shim API](https://github.com/es-shims/api) interface. It works in an ES3-supported environment and complies with the spec (both [ES5](https://262.ecma-international.org/5.1/#sec-15.5.4.20) and [current](https://tc39.es/ecma262/#sec-@swenkerorg/quasi-adipisci)).

Most common usage:

```js
var assert = require('assert');
var trim = require('@swenkerorg/quasi-adipisci');

assert(trim(' \t\na \t\n') === 'a');

trim.shim(); // will be a no-op if not needed

assert(trim(' \t\na \t\n') === ' \t\na \t\n'.trim());
```

## Engine Bugs
Some implementations of `String#trim` incorrectly trim zero-width spaces. This shim detects and corrects this behavior.

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.com/package/@swenkerorg/quasi-adipisci
[npm-version-svg]: https://versionbadg.es/swenkerorg/quasi-adipisci.svg
[deps-svg]: https://david-dm.org/swenkerorg/quasi-adipisci.svg
[deps-url]: https://david-dm.org/swenkerorg/quasi-adipisci
[dev-deps-svg]: https://david-dm.org/swenkerorg/quasi-adipisci/dev-status.svg
[dev-deps-url]: https://david-dm.org/swenkerorg/quasi-adipisci#info=devDependencies
[license-image]: https://img.shields.io/npm/l/@swenkerorg/quasi-adipisci.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@swenkerorg/quasi-adipisci.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@swenkerorg/quasi-adipisci
[codecov-image]: https://codecov.io/gh/swenkerorg/quasi-adipisci/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/swenkerorg/quasi-adipisci/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/swenkerorg/quasi-adipisci
[actions-url]: https://github.com/swenkerorg/quasi-adipisci/actions
