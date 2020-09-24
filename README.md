# blockchain-notes

## Ethereum

### Truffle
https://www.npmjs.com/package/truffle

Truffle is the CLI to deploy and run tests

Useful Commands
```sol
truffle compile

truffle console

truffle migrate --reset // deploy the new contract

truffle test
```

### Ganache
Ganache is an in memory blockchain used to for testing

### Solidity

* External Vs Public - External is for external only calls, public is for both external and internal calls (More gas)

### Geth
Geth is a go version of ethereum

Running Geth on rinkeby
```bash
geth --rinkeby --rpc --rpcapi="personal,eth,network,web3,net" --ipcpath="~/Library/Ethereum/geth.ipc"
```


