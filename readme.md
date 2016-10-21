# p-pipe [![Build Status](https://travis-ci.org/sindresorhus/p-pipe.svg?branch=master)](https://travis-ci.org/sindresorhus/p-pipe)

> Compose promise-returning & async functions into a reusable pipeline


## Install

```
$ npm install --save p-pipe
```


## Usage

```js
const pPipe = require('p-pipe');

const addUnicorn = str => Promise.resolve(`${str} Unicorn`);
const addRainbow = str => Promise.resolve(`${str} Rainbow`);

const pipeline = pPipe(addUnicorn, addRainbow);

pipeline('❤️').then(console.log);
//=> '❤️ Unicorn Rainbow'
```


## API

### pPipe(input, …)

The `input` functions are applied from left to right.

#### input

Type: `Function`

Expected to return a `Promise` or any value.


## Related

- [p-each-series](https://github.com/sindresorhus/p-each-series) - Iterate over promises serially
- [More…](https://github.com/sindresorhus/promise-fun)


## License

MIT © [Sindre Sorhus](https://sindresorhus.com)