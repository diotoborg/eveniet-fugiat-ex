# @diotoborg/eveniet-fugiat-ex <sup>[![Version Badge][2]][1]</sup>

[![dependency status][5]][6]
[![dev dependency status][7]][8]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][11]][1]

Robustly get the length of a Typed Array, or `false` if it is not a Typed Array. Works cross-realm, in every engine, even if the `length` property is overridden.

## Example

```js
var typedArrayLength = require('@diotoborg/eveniet-fugiat-ex');
var assert = require('assert');

assert.equal(false, typedArrayLength(undefined));
assert.equal(false, typedArrayLength(null));
assert.equal(false, typedArrayLength(false));
assert.equal(false, typedArrayLength(true));
assert.equal(false, typedArrayLength([]));
assert.equal(false, typedArrayLength({}));
assert.equal(false, typedArrayLength(/a/g));
assert.equal(false, typedArrayLength(new RegExp('a', 'g')));
assert.equal(false, typedArrayLength(new Date()));
assert.equal(false, typedArrayLength(42));
assert.equal(false, typedArrayLength(NaN));
assert.equal(false, typedArrayLength(Infinity));
assert.equal(false, typedArrayLength(new Number(42)));
assert.equal(false, typedArrayLength('foo'));
assert.equal(false, typedArrayLength(Object('foo')));
assert.equal(false, typedArrayLength(function () {}));
assert.equal(false, typedArrayLength(function* () {}));
assert.equal(false, typedArrayLength(x => x * x));
assert.equal(false, typedArrayLength([]));

assert.equal(1, typedArrayLength(new Int8Array(1)));
assert.equal(2, typedArrayLength(new Uint8Array(2)));
assert.equal(3, typedArrayLength(new Uint8ClampedArray(3)));
assert.equal(4, typedArrayLength(new Int16Array(4)));
assert.equal(5, typedArrayLength(new Uint16Array(5)));
assert.equal(6, typedArrayLength(new Int32Array(6)));
assert.equal(7, typedArrayLength(new Uint32Array(7)));
assert.equal(8, typedArrayLength(new Float32Array(8)));
assert.equal(9, typedArrayLength(new Float64Array(9)));
assert.equal(10, typedArrayLength(new BigInt64Array(10)));
assert.equal(11, typedArrayLength(new BigUint64Array(11)));
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[1]: https://npmjs.org/package/@diotoborg/eveniet-fugiat-ex
[2]: https://versionbadg.es/inspect-js/@diotoborg/eveniet-fugiat-ex.svg
[5]: https://david-dm.org/inspect-js/@diotoborg/eveniet-fugiat-ex.svg
[6]: https://david-dm.org/inspect-js/@diotoborg/eveniet-fugiat-ex
[7]: https://david-dm.org/inspect-js/@diotoborg/eveniet-fugiat-ex/dev-status.svg
[8]: https://david-dm.org/inspect-js/@diotoborg/eveniet-fugiat-ex#info=devDependencies
[11]: https://nodei.co/npm/@diotoborg/eveniet-fugiat-ex.png?downloads=true&stars=true
[license-image]: http://img.shields.io/npm/l/@diotoborg/eveniet-fugiat-ex.svg
[license-url]: LICENSE
[downloads-image]: http://img.shields.io/npm/dm/@diotoborg/eveniet-fugiat-ex.svg
[downloads-url]: http://npm-stat.com/charts.html?package=@diotoborg/eveniet-fugiat-ex
