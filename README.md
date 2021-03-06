# JSON-typescript <a href="https://travis-ci.org/mike-north/json-typescript"  align='right'><img src="https://travis-ci.org/mike-north/json-typescript.svg?branch=master"></a>
TypeScript type information for compile-time validation of [JSON objects](https://www.json.org/).

[![Greenkeeper badge](https://badges.greenkeeper.io/mike-north/json-typescript.svg)](https://greenkeeper.io/)

## How to use this

1. Install this package
```js
npm install --save-dev json-typescript
```

2. Import this package
```ts
import _JSON from 'json-typescript';
```

3. Check to see if json types are validated correctly

```ts
import _JSON from 'json-typescript';

// ✅ This should be OK
let doc: _JSON.Value = {
  data: {
    type: 'articles',
    id: '1'
  }
};

// ⛔️ This should NOT be OK ( functions are not allowed )
let doc: _JSON.Value = {
  foo() {
    return bar;
  }
};

// ⛔️ This should NOT be OK ( Array is not a JSON.Object )
let doc: _JSON.Object = [];
```

## Copyright
&copy; 2018 [Mike North](https://github.com/mike-north), All Rights Reserved.
