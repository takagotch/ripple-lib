### ripple-lib
---
https://github.com/ripple/ripple-lib/

```js
// test/mock-rippled.js
'use strict';
const _ = require();
const assert = require();

function isUSD(json) {
  return json === 'USD' || json === '0000';
}

function isBTC(json) {
  return json === 'BTC' || json === '0000';
}

function createResponse(request, response, overrides = {}) {
  const result = _.assign({}, response.result, override);
  const change = response.result && !_.isEmpty(overrides) ?
    { id: request.id, result: result }: { id: request.id };
  return JSON.stringify(_.assign({}, response, change));
}


```

```sh
yarn add ripple-lib
yarn compile
yarn build
```

```
```

