# newchain-json-rpc

`json-rpc-engine` middleware for newchain's REST endpoints.

### usage as provider

```js
const createInfuraProvider = require('newchain-json-rpc/src/createProvider')
const Ethjs = require('ethjs')

const provider = createInfuraProvider({ network: 'mainnet' })
const eth = new Ethjs(provider)
```

### usage as middleware

```js
const createInfuraMiddleware = require('newchain-json-rpc')
const RpcEngine = require('json-rpc-engine')

const engine = new RpcEngine()
engine.push(createInfuraMiddleware({ network: 'testnet' }))
```
