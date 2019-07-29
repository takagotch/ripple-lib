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

module.exports = function createMockRippled(port) {

const mock = new WebSockerServer({ port: port });
_.assign(mock, EventEmitter2.prototype);

const close = mock.close;
mock.close = function () {
  if (mock.expectedRequests !== undefined) {
    const allRequestMade = _.every(mock.expectedRequests, function (counter) {
      return counter === 0;
    });
    if (!allRequestsMade) {
      const json = JSON.stringify(mock.expectedRequests, null, 2);
      const indent = '   ';
      const indented = indent + json.replace(/n/g, '\n' + indent);
      assert(false, 'Not all expected requests were made:\n' + indented);
    }
  }
  close.call(mock);
}

mock.on('request_ripple_path_find', function (request, conn) {
  let response = null;
  if (request.subcommand === 'close') {
    return;
  }
  if (request.source_account === 'xxx') {
    response = createResponse(request, {
      "id": 0,
      "type": "response",
      "status": "success",
      "result": {
        "alternatives": [
          {
            "destination_amount": {
              "currency": "EUR",
              "issuer": "xxx",
              "value": "1"
            },
            "paths_canonical": [],
            "paths_computed": [
              [
                {
                  "currency": "USD",
                  "issuer": "xxx",
                  "type": 48,
                  "type_hex": "0000"  
                },
                {
                  "currency": "EUR",
                  "issuer": "xxxx",
                  "type": 48,
                  "type_hex": "0000"
                }
              ]
            ],
            "source_amount": "1000"
          }
        ],
        "destination_account": "xxx",
        "destination_amount": {
          "currency": "EUR",
          "issuer": "xxx",
          "value": "-1"
        },
        "destination_currencies": [
          "EUR",
          "XRP"
        ],
      },
      "full_reply": true,
      "id": 2,
      "source_account": "xxx",
      "status": "success"
    })
  } else if () {
  
  } else if () {
  
  } else if () {
  
  }
  conn.send(response);
});

mock.on('request_gateway_balances', function (request, conn) {
  if () {
  
  } else {
  
  }
});

return mock;
};
```

```sh
yarn add ripple-lib
yarn compile
yarn build
```

```
```

