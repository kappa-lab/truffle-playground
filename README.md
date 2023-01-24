# Require
- [Truffle](https://trufflesuite.com/docs/truffle/)
- [Ganache](https://trufflesuite.com/docs/ganache/)

# Create Project
```sh
truffle unbox metacoin my_prj
```

# Compile
```sh
truffle compile
```

# Link Truffle Project
- https://trufflesuite.com/docs/ganache/how-to/link-a-truffle-project/

# Deploy SmartContract
```sh
truffle deploy
```
# Exec SmartContract

### Start Console
```sh
truffle console 
```

### In Console
Show Accounts
```js
truffle(ganache)>let accounts = await web3.eth.getAccounts()
truffle(ganache)>accounts
[
  '0x5cb4F50c1672432a5a8ee9A3eb6086AcbC74625a',
  '0x30BC44b4F8EC5Ee5b0d238d962223127428D0e1c',
  '0xF0E528D29481245dF6edFF420aA1604FFcd7C08e',
  '0xb9E296be74a986Ff0b834E81dc8080D07867cB0f',
  '0x15B4c6aAfe4c2abc63946eB12F70f14323c2d43A',
  '0xa627214ECfD4E2d56DF56a423D769DdE582899E0',
  '0x3705B9B8A57D710495BE99E7400d996319010360',
  '0xD714e4146dF1dB5A1417a4dE569Ac978e41028Db',
  '0x16Ab6239F4d339E05C55dEb1EBf553295b3f81C0',
  '0x49823b63e4DcfDC96cc7F99aC1eB1ccb307E8653'
]
```

Show Balance
```js
instance.getBalance('0x5cb4F50c1672432a5a8ee9A3eb6086AcbC74625a')
BN {
  negative: 0,
  words: [ 10000, <1 empty item> ],
  length: 1,
  red: null
}
```

Send Coin
```js
truffle(ganache)> instance.sendCoin('0x30BC44b4F8EC5Ee5b0d238d962223127428D0e1c',1)
{
  tx: '0xe40a9dbe27a144e1d6a344020178e60440915556abe099d5ae67a74d2c5f6c76',
  receipt: {
    transactionHash: '0xe40a9dbe27a144e1d6a344020178e60440915556abe099d5ae67a74d2c5f6c76',
    transactionIndex: 0,
    blockHash: '0xbeb310c6309511ae2435a2a6f537089fe7c4740c72d4d8fe1c03b7da91bed2d6',
    blockNumber: 3,
    from: '0x5cb4f50c1672432a5a8ee9a3eb6086acbc74625a',
    to: '0x5ff88a8e749af0627d0a1fc01a199b08cbdc2cc3',
    gasUsed: 52485,
    cumulativeGasUsed: 52485,
    contractAddress: null,
    logs: [ [Object] ],
    status: true,
    logsBloom: '0x00000000000000000000000000080000000000000000000000000000000000100000000000000000000000000000000000000000400000000000000000000000000000000000000000000008000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000000000000000000000004000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000100080000',
    rawLogs: [ [Object] ]
  },
  logs: [
    {
      logIndex: 0,
      transactionIndex: 0,
      transactionHash: '0xe40a9dbe27a144e1d6a344020178e60440915556abe099d5ae67a74d2c5f6c76',
      blockHash: '0xbeb310c6309511ae2435a2a6f537089fe7c4740c72d4d8fe1c03b7da91bed2d6',
      blockNumber: 3,
      address: '0x5FF88A8e749AF0627D0a1fC01A199b08CBdC2Cc3',
      type: 'mined',
      id: 'log_f3828177',
      event: 'Transfer',
      args: [Result]
    }
  ]
}
```

Show Balance
```js
truffle(ganache)> instance.getBalance('0x5cb4F50c1672432a5a8ee9A3eb6086AcbC74625a')
BN {
  negative: 0,
  words: [ 9999, <1 empty item> ],
  length: 1,
  red: null
}
truffle(ganache)> instance.getBalance('0x5cb4F50c1672432a5a8ee9A3eb6086AcbC74625a')
BN {
  negative: 0,
  words: [ 9999, <1 empty item> ],
  length: 1,
  red: null
}```