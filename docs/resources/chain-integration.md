# Cronos Integration documentation

## Useful Links

- [Cronos website](https://cronos.org/)
- [GitHub Repository](https://github.com/crypto-org-chain/cronos)
- [Official Documentation](https://cronos.org/docs/)
- [Cronos Binaries](https://github.com/crypto-org-chain/cronos/releases)

## Integration guide for **Cronos Mainnet Beta**

### Setup Guide

- [Joining the Cronos Mainnet](https://cronos.org/docs/getting-started/cronos-mainnet.html)
- [Deploying Smart Contract](https://cronos.org/docs/getting-started/cronos-smart-contract.html)
- [Seeds for Fullnode](https://github.com/crypto-org-chain/cronos-mainnet#seed-nodes)
- [Genesis files](https://raw.githubusercontent.com/crypto-org-chain/cronos-mainnet/master/cronosmainnet_25-1/genesis.json)
- [JSON-RPC Swagger Playground](https://cronos.org/swagger?network=mainnet)
- [Using MetaMask](https://cronos.org/docs/getting-started/metamask.html)

### RPC URLs for Cronos mainnet Beta

:::danger Public RPCs URL Updates:
The Cronos RPC endpoints have been lately updated (shown as below) and it is recommended for users to update the endpoints. The old endpoints are still available for compatibility but maybe deprecated later.
:::

:::tip Request Limits on Public RPCs:
To provide a stable experience to users, there is a request rate limit on the public RPCs to ensure fair usage. If your application requires a higher usage, please consider setting up your own nodes. You can also reach out to us on [Discord](https://discord.gg/cGtxgVfGMZ) for assistance.
:::

:::tip Public RPCs Integration Tips:
There are more than one machines serving the public RPC services. There is no guarantee that you are served by the same machine every time. This could break the assumptions of some applications. For example when you want to broadcast multiple transactions in sequential account nonce at once, each transactions may arrive on different machines if you are not broadcasting them in a batch.

If this assumption is important in your application, please consider setting up your own nodes.
:::

1. **Tendermint RPC**

   - [https://rpc.cronos.org/](https://rpc.cronos.org/)

2. **Cosmos RESTful**

   - [https://rest.cronos.org/](https://rest.cronos.org/)

3. **Cosmos gRPC Based**

   - [https://grpc.cronos.org/](http://grpc.cronos.org/)

4. **EVM HTTP JSON RPC (Web3 compatible)**
   - [https://evm.cronos.org/](https://evm.cronos.org/)

## Official token contract addresses for Cronos mainnet Beta

Below is the preview of the [complete list of the official token contract addresses](https://github.com/crypto-org-chain/cronos-docs/tree/master/docs/resources/token-contract-addresses.md).

| Token name | Address                                                                                                                               | Decimal |
| ---------- | ------------------------------------------------------------------------------------------------------------------------------------- | ------- |
| WCRO       | [0x5C7F8A570d578ED84E63fdFA7b1eE72dEae1AE23](https://cronoscan.com/tokens/0x5C7F8A570d578ED84E63fdFA7b1eE72dEae1AE23/token-transfers) | 18      |
| WETH       | [0xe44Fd7fCb2b1581822D0c862B68222998a0c299a](https://cronoscan.com/tokens/0xe44Fd7fCb2b1581822D0c862B68222998a0c299a/token-transfers) | 18      |
| WBTC       | [0x062E66477Faf219F25D27dCED647BF57C3107d52](https://cronoscan.com/tokens/0x062E66477Faf219F25D27dCED647BF57C3107d52/token-transfers) | 8       |
| USDC       | [0xc21223249CA28397B4B6541dfFaEcC539BfF0c59](https://cronoscan.com/tokens/0xc21223249CA28397B4B6541dfFaEcC539BfF0c59/token-transfers) | 6       |
| USDT       | [0x66e428c3f67a68878562e79A0234c1F83c208770](https://cronoscan.com/tokens/0x66e428c3f67a68878562e79A0234c1F83c208770/token-transfers) | 6       |
| DAI        | [0xF2001B145b43032AAF5Ee2884e456CCd805F677D](https://cronoscan.com/tokens/0xF2001B145b43032AAF5Ee2884e456CCd805F677D/token-transfers) | 18      |



## Integration guide for **Cronos Testnet**

### Setup Guide

- [Joining the Cronos Testnet](https://cronos.org/docs/getting-started/cronos-testnet.html)
- [Testnet Faucet](https://cronos.org/faucet/)
  - Note that the faucet only takes eth-type `0x...` addr
- [Seeds for fullnode](https://github.com/crypto-org-chain/cronos-testnets/blob/main/testnet.json#L21)
- [Genesis files](https://raw.githubusercontent.com/crypto-org-chain/cronos-testnets/main/cronostestnet_338-1/genesis.json)
- [JSON-RPC Swagger Playground](https://cronos.org/swagger)
- Using Metamask for testnet
  - Network Name: **Cronos Testnet**
  - New RPC URL: **https://evm-t3.cronos.org/**
  - Chain ID: **338**
  - Currency Symbol: **TCRO**
  - Block Explorer URL: **https://testnet.cronoscan.com/**

### RPC URLs for For Cronos testnet

:::tip
The Cronos Testnet RPC endpoints have been lately updated shown as below and it is recommanded for users to update the endpoints, while the old endpoints will still be compatible.
:::

1. **Cosmos RPC**

   - https://rpc-t3.cronos.org/

2. **gRPC Based**

   - https://grpc-t3.cronos.org/

3. **Cosmos RESTful**

   - https://rest-t3.cronos.org/

4. **EVM HTTP JSON RPC**

   - https://evm-t3.cronos.org/

### Mock token contract addresses for Cronos testnet

| Token name | address                                      | decimal |
| ---------- | -------------------------------------------- | ------- |
| WCRO       | `0x6a3173618859C7cd40fAF6921b5E9eB6A76f1fD4` | 18      |
| WETH       | `0x796135E94527c38433e9c42f4Cd91ca931E5e6A6` | 18      |
| WBTC       | `0xEE200f25d7B1B9518AC944fd60b113d39bee209c` | 8       |
| USDC       | `0x25f0965F285F03d6F6B3B21c8EC3367412Fd0ef6` | 6       |
| USDT       | `0xa144617Afd9205AF1ceDE3Cc671da1a409A82c5a` | 6       |
| DAI        | `0x8662A8111daEC7570a1bDF3dbd3E163d41563904` | 18      |

## API Clients and libraries

- [**TypeScript** library](https://github.com/crypto-org-chain/chain-jslib);
- [**Python** library](https://pypi.org/project/chainlibpy/#description);
- [**Rust** library](https://github.com/crypto-org-chain/chainlib-rs) (note that it is not feature complete);
- [@cosmjs/stargate](https://github.com/cosmos/cosmjs/tree/master/packages/stargate).

# Ethereum type JSON-RPC Methods

### Pre-requisite Readings

- [Ethereum JSON-RPC](https://eth.wiki/json-rpc/API) {prereq}
- [Geth JSON-RPC APIs](https://geth.ethereum.org/docs/rpc/server) {prereq}

Below is a list of Ethereum type JSON-RPC Methods where users can curl via local node. While you can also surf to our swagger playground for a better understanding.

- [Mainnet swagger playground](https://cronos.org/swagger?network=mainnet)
- [Testnet swagger playground](https://cronos.org/swagger)

### JSON-RPC Methods

| Method                                                                            | Namespace | Implemented | Public |
| --------------------------------------------------------------------------------- | --------- | ----------- | ------ |
| [`web3_clientVersion`](#web3-clientversion)                                       | Web3      | ✔           | ✔      |
| [`web3_sha3`](#web3-sha3)                                                         | Web3      | ✔           | ✔      |
| [`net_version`](#net-version)                                                     | Net       | ✔           | ✔      |
| [`net_peerCount`](#net-peerCount)                                                 | Net       | ✔           | ✔      |
| [`net_listening`](#net-listening)                                                 | Net       | ✔           | ✔      |
| [`eth_protocolVersion`](#eth-protocolversion)                                     | Eth       | ✔           | ✔      |
| [`eth_syncing`](#eth-syncing)                                                     | Eth       | ✔           | ✔      |
| [`eth_gasPrice`](#eth-gasprice)                                                   | Eth       | ✔           | ✔      |
| [`eth_accounts`](#eth-accounts)                                                   | Eth       | ✔           | ✔      |
| [`eth_blockNumber`](#eth-blocknumber)                                             | Eth       | ✔           | ✔      |
| [`eth_getBalance`](#eth-getbalance)                                               | Eth       | ✔           | ✔      |
| [`eth_getStorageAt`](#eth-getstorageat)                                           | Eth       | ✔           | ✔      |
| [`eth_getTransactionCount`](#eth-gettransactioncount)                             | Eth       | ✔           | ✔      |
| [`eth_getBlockTransactionCountByNumber`](#eth-getblocktransactioncountbynumber)   | Eth       | ✔           | ✔      |
| [`eth_getBlockTransactionCountByHash`](#eth-getblocktransactioncountbyhash)       | Eth       | ✔           | ✔      |
| [`eth_getCode`](#eth-getcode)                                                     | Eth       | ✔           | ✔      |
| [`eth_sign`](#eth-sign)                                                           | Eth       | ✔           | ✔      |
| [`eth_sendTransaction`](#eth-sendtransaction)                                     | Eth       | ✔           | ✔      |
| [`eth_sendRawTransaction`](#eth-sendrawtransaction)                               | Eth       | ✔           | ✔      |
| [`eth_call`](#eth-call)                                                           | Eth       | ✔           | ✔      |
| [`eth_estimateGas`](#eth-estimategas)                                             | Eth       | ✔           | ✔      |
| [`eth_getBlockByNumber`](#eth-getblockbynumber)                                   | Eth       | ✔           | ✔      |
| [`eth_getBlockByHash`](#eth-getblockbyhash)                                       | Eth       | ✔           | ✔      |
| [`eth_getTransactionByHash`](#eth-gettransactionbyhash)                           | Eth       | ✔           | ✔      |
| [`eth_getTransactionByBlockHashAndIndex`](#eth-gettransactionbyblockhashandindex) | Eth       | ✔           | ✔      |
| [`eth_getTransactionReceipt`](#eth-gettransactionreceipt)                         | Eth       | ✔           | ✔      |
| [`eth_newFilter`](#eth-newfilter)                                                 | Eth       | ✔           | ✔      |
| [`eth_newBlockFilter`](#eth-newblockfilter)                                       | Eth       | ✔           | ✔      |
| [`eth_newPendingTransactionFilter`](#eth-newpendingtransactionfilter)             | Eth       | ✔           | ✔      |
| [`eth_uninstallFilter`](#eth-uninstallfilter)                                     | Eth       | ✔           | ✔      |
| [`eth_getFilterChanges`](#eth-getfilterchanges)                                   | Eth       | ✔           | ✔      |
| [`eth_getFilterLogs`](#eth-getfilterlogs)                                         | Eth       | ✔           | ✔      |
| [`eth_getLogs`](#eth-getlogs)                                                     | Eth       | ✔           | ✔      |
| `eth_getTransactionbyBlockNumberAndIndex`                                         | Eth       |             | ✔      |
| `eth_submitHashrate`                                                              | Eth       |             |        |
| `eth_getCompilers`                                                                | Eth       |             |        |
| `eth_compileLLL`                                                                  | Eth       |             |        |
| `eth_compileSolidity`                                                             | Eth       |             |        |
| `eth_compileSerpent`                                                              | Eth       |             |        |
| `eth_signTransaction`                                                             | Eth       |             |        |
| [`eth_coinbase`](#eth-coinbase)                                                   | Eth       | ✔           |        |
| [`eth_getProof`](#eth-getProof)                                                   | Eth       | ✔           |        |
| [`eth_subscribe`](#eth-subscribe)                                                 | Websocket | ✔           |        |
| [`eth_unsubscribe`](#eth-unsubscribe)                                             | Websocket | ✔           |        |

:::tip
Block Number can be entered as a Hex string, `"earliest"`, `"latest"` or `"pending"`.
:::
:::tip
While the examples below make use of local node http://localhost:8545, users may also use our public full node:
https://evm-t3.cronos.org:8545/
:::

## JSON-RPC namespaces

### Pre-requisite Readings

- [Geth JSON-RPC Namespaces](https://geth.ethereum.org/docs/rpc/server) {prereq}

### Ethereum Namespaces

| Namespace                                     | Description                                                                                                                                                                                                                  | Supported | Enabled by Default |
| --------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | ------------------ |
| [`eth`](./endpoints.md#eth-methods)           | Cronos provides several extensions to the standard `eth` JSON-RPC namespace.                                                                                                                                                 | ✔         | ✔                  |
| [`web3`](./endpoints.md#web3-methods)         | The `web3` API provides utility functions for the web3 client.                                                                                                                                                               | ✔         | ✔                  |
| [`net`](./endpoints.md#net-methods)           | The `net` API provides access to network information of the node                                                                                                                                                             | ✔         | ✔                  |
| `clique`                                      | The `clique` API provides access to the state of the clique consensus engine. You can use this API to manage signer votes and to check the health of a private network.                                                      | ❌        |                    |
| `debug`                                       | The `debug` API gives you access to several non-standard RPC methods, which will allow you to inspect, debug and set certain debugging flags during runtime.                                                                 | ✔         |                    |
| `les`                                         | The `les` API allows you to manage LES server settings, including client parameters and payment settings for prioritized clients. It also provides functions to query checkpoint information in both server and client mode. | ❌        |                    |
| [`miner`](./endpoints.md#miner-methods)       | The `miner` API allows you to remote control the node’s mining operation and set various mining specific settings.                                                                                                           | ✔         | ❌                 |
| [`txpool`](./endpoints.md#txpool-methods)     | The `txpool` API gives you access to several non-standard RPC methods to inspect the contents of the transaction pool containing all the currently pending transactions as well as the ones queued for future processing.    | ✔         | ❌                 |
| `admin`                                       | The `admin` API gives you access to several non-standard RPC methods, which will allow you to have a fine grained control over your nodeinstance, including but not limited to network peer and RPC endpoint management.     | ❌        |                    |
| [`personal`](./endpoints.md#personal-methods) | The `personal` API manages private keys in the key store.                                                                                                                                                                    | ✔         | ❌                 |

## Block Explorer

- Cronos Mainnet Beta:
  [https://cronoscan.com/](https://cronoscan.com)
- Cronos Testnet:
  [https://testnet.cronoscan.com/](https://testnet.cronoscan.com/)

### Creating API Keys on CronoScan
The CronoScan Developer APIs are designed to provide accessible and consistent Cronos data to the Cronos community. 
The APIs are provided as a community service with a rate up to 5 calls per second per IP. 
Users need to [register](https://cronoscan.com/register) for a CronoScan account to create an API key. 
After registration, a CronoScan user account will have a quota of up to 3 API keys.

On the [CronoScan user dashboard](https://cronoscan.com/myaccount), select “_**API-KEYs**_” from the left-hand side column or go to [https://cronoscan.com/myapikey](https://cronoscan.com/myapikey).

<p align="center">
<img src="./assets/myapikey-page.png" alt="drawing" height="400px"/>
</p>

Click on the “_**Create a new API-KEY token**_” button, then optionally input an “_**AppName**_”, “My Cronos App” for example.

<p align="center">
<img src="./assets/create-apikey.png" alt="drawing" height="200px"/>
</p>

After the “_**API-KEY Token**_” is successfully created, a message will show up as below, and you may now use the “_**API key token**_” for your applications on Cronos!

<p align="center">
<img src="./assets/create-apikey-successful.png" alt="drawing" height="300px"/>
</p>

## Community

[Discord](https://discord.gg/cGtxgVfGMZ)
