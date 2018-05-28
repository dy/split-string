# split-string-by [![unstable](https://img.shields.io/badge/stability-unstable-orange.svg)](http://github.com/badges/stability-badges) [![Build Status](https://img.shields.io/travis/dy/split-string-by.svg)](https://travis-ci.org/dy/split-string-by)

Split string by a separator with respect to brackets, quotes and escape markers. Optimized version of [string-split](https://github.com/jonschlinkert/split-string).

## Usage

[![npm install split-string-by](https://nodei.co/npm/split-string-by.png?mini=true)](https://npmjs.org/package/split-string-by/)


```js
var split = require('split-string-by')

split('a."b.c".d.{.e.f.g.}.h', '.')
// ['a', '"b.c"', 'd', '{.e.f.g.}', 'h']

split('a."b.c".d.{.e.f.g.}.h', '.', {ignore: '""'})
// ['a', '"b.c"', 'd', '{', 'e', 'f', 'g', '}', 'h']
```

## API

### parts = splitBy(string, separator, opts?)

Return array with tokens.

Option | Default | Meaning
---|---|---
`ignore` | `['"', "'", '\`', '“”', '«»', '[]', '()', '{}']` | Avoid splitting content enclosed in the character pairs. Can be a string or a list of strings.
`escape` | `true` | Avoid splitting at the escaped separator, eg. `\.` won't be separated by `'.'` separator.


## Related

* [parenthesis](http://npmjs.org/package/parenthesis)

## License

© 2018 Dmitry Yv. MIT License
