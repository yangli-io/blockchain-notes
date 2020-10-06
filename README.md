# blockchain-notes

## Ethereum

### Truffle
https://www.npmjs.com/package/truffle

Truffle is the CLI to deploy and run tests

Useful Commands
```bash
truffle compile

truffle console

truffle migrate --reset // deploy the new contract

truffle test

truffle migrate --reset --compile-all --network rinkeby
```

### Ganache
Ganache is an in memory blockchain used to for testing

### Geth
Geth is a go version of ethereum

Running Geth on rinkeby
```bash
geth --rinkeby --rpc --allow-insecure-unlock --rpcapi="personal,eth,network,web3,net" --ipcpath="~/Library/Ethereum/geth.ipc"
```

```bash
geth attach // Console

geth --rinkeby account new // Creates new account
```

Commands in Console
```bash
eth.syncing // Get the current blocks;
```

rinkeby.etherscan.io

faucet.rinkeby.io
