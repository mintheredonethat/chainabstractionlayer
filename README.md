# Chain Abstraction Layer <img align="right" src="./liquality-logo.png" height="80px" />

[![ChainAbstractionLayer](https://travis-ci.org/liquality/chainabstractionlayer.svg?branch=master)](https://travis-ci.org/liquality/chainabstractionlayer)
[![Standard Code Style](https://img.shields.io/badge/codestyle-standard-brightgreen.svg)](https://github.com/standard/standard)
[![MIT License](https://img.shields.io/badge/license-MIT-brightgreen.svg)](./LICENSE.md)
[![ChainAbstractionLayer](https://img.shields.io/npm/dt/chainabstractionlayer.svg)](https://npmjs.com/package/chainabstractionlayer)

> :warning: This project is under heavy development. Expect bugs & breaking changes.

Query different blockchains with a single and simple interface.

[Introductory Blog Post](https://medium.com/liquality/the-missing-tool-to-cross-chain-development-2ebfe898efa1)

## Installation

```bash
npm install @liquality/chainabstractionlayer
```

> **Error: Cannot find module 'babel-runtime/core-js/get-iterator'**
>
> Issues to track: [LedgerHQ/ledgerjs/issues/211](https://github.com/LedgerHQ/ledgerjs/issues/211), [LedgerHQ/ledgerjs/issues/218](https://github.com/LedgerHQ/ledgerjs/issues/218)
>
> `npm install babel-runtime`


## Usage

```javascript
import { Client, providers } from '@liquality/chainabstractionlayer'

const { BitcoinRPCProvider } = providers.bitcoin

const bitcoin = new Client()
bitcoin.addProvider(new BitcoinRPCProvider('http://localhost:8080', 'bitcoin', 'local321'))

bitcoin
  .generateBlock(1) // returns Promise
  .then(console.log) // Array<BlockHash>
```

## Community

[Liquality Gitter](https://gitter.im/liquality/Lobby?source=orgpage)

### Try ChainAbstractionLayer in Browser

<table>
  <thead>
    <tr>
      <th>Chain</th>
      <th>Wallet Provider</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan=2>Ethereum</td>
      <td>Ledger</td>
      <td>
        <a href="./examples/browser/ethereum/ledger.html">Source</a>
        &amp;
        <a href="https://liquality.github.io/chainabstractionlayer/examples/browser/ethereum/ledger.html">Demo</a>
      </td>
    </tr>
    <tr>
      <td>MetaMask</td>
      <td>
        <a href="./examples/browser/ethereum/metamask.html">Source</a>
        &amp;
        <a href="https://liquality.github.io/chainabstractionlayer/examples/browser/ethereum/metamask.html">Demo</a>
      </td>
    </tr>
    <tr>
      <td>Bitcoin</td>
      <td>Ledger</td>
      <td>
        <a href="./examples/browser/bitcoin/ledger.html">Source</a>
        &amp;
        <a href="https://liquality.github.io/chainabstractionlayer/examples/browser/bitcoin/ledger.html">Demo</a>
      </td>
    </tr>
  </tbody>
</table>


## Documentation

The documentation is being generated by [esdoc](https://www.npmjs.com/package/esdoc). Github Page hosted documentation is available at [liquality.github.io/chainabstractionlayer](https://liquality.github.io/chainabstractionlayer/)

If you want to build documentation locally;

```bash
npm run build:docs
```


## License

[MIT](./LICENSE.md)
