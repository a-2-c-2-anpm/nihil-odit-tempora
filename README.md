# @a-2-c-2-anpm/nihil-odit-tempora <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Is this value a JS WeakMap? This module works cross-realm/iframe, and despite ES6 @@toStringTag.

## Example

```js
var isWeakMap = require('@a-2-c-2-anpm/nihil-odit-tempora');
assert(!isWeakMap(function () {}));
assert(!isWeakMap(null));
assert(!isWeakMap(function* () { yield 42; return Infinity; });
assert(!isWeakMap(Symbol('foo')));
assert(!isWeakMap(1n));
assert(!isWeakMap(Object(1n)));

assert(!isWeakMap(new Set()));
assert(!isWeakMap(new WeakSet()));
assert(!isWeakMap(new Map()));

assert(isWeakMap(new WeakMap()));

class MyWeakMap extends WeakMap {}
assert(isWeakMap(new MyWeakMap()));
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/@a-2-c-2-anpm/nihil-odit-tempora
[npm-version-svg]: https://versionbadg.es/inspect-js/@a-2-c-2-anpm/nihil-odit-tempora.svg
[deps-svg]: https://david-dm.org/inspect-js/@a-2-c-2-anpm/nihil-odit-tempora.svg
[deps-url]: https://david-dm.org/inspect-js/@a-2-c-2-anpm/nihil-odit-tempora
[dev-deps-svg]: https://david-dm.org/inspect-js/@a-2-c-2-anpm/nihil-odit-tempora/dev-status.svg
[dev-deps-url]: https://david-dm.org/inspect-js/@a-2-c-2-anpm/nihil-odit-tempora#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@a-2-c-2-anpm/nihil-odit-tempora.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@a-2-c-2-anpm/nihil-odit-tempora.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@a-2-c-2-anpm/nihil-odit-tempora.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@a-2-c-2-anpm/nihil-odit-tempora
[codecov-image]: https://codecov.io/gh/inspect-js/@a-2-c-2-anpm/nihil-odit-tempora/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/inspect-js/@a-2-c-2-anpm/nihil-odit-tempora/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/inspect-js/@a-2-c-2-anpm/nihil-odit-tempora
[actions-url]: https://github.com/a-2-c-2-anpm/nihil-odit-tempora/actions
