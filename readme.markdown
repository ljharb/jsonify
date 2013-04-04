# jsonify

This module provides Douglas Crockford's JSON implementation without modifying
any globals.

`stringify` and `parse` are merely exported without respect to whether or not a
global `JSON` object exists.

[![build status](https://secure.travis-ci.org/substack/jsonify.png)](http://travis-ci.org/substack/jsonify)

# methods

``` js
var json = require('jsonify');
```

## json.parse(source, reviver)

Return a new javascript object from a parse of the `source` string.

If a `reviver` function is specified, walk the structure passing each name/value
pair to `reviver.call(parent, key, value)` to transform the `value` before
parsing it.

## json.stringify(value, replacer, space)

Return a string representation for `value`.

If `replacer` is specified, walk the structure passing each name/value pair to
`replacer.call(parent, key, value)` to transform the `value` before stringifying
it.

If `space` is a number, indent the result by that many spaces.
If `space` is a string, use `space` as the indentation.

# install

With [npm](http://npmjs.org) do:

```
npm install jsonify
```

To use this module in the browser, check out
[browserify](https://github.com/substack/node-browserify).

# license

public domain
