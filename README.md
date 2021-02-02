# Start With Grin

```
The Four Agreements:

Be Impeccable With Your Word 
Don't Take Anything Personally
Don't Make Assumptions
Always Do Your Best
```

## Walk Through: Create Local Grin Development Enviroment

This walkthough will create an enviroment is useful if you want to develop with grin locally.

**Note:**

- `chain_type` in your `grin-wallet.toml` and `grin-node.toml` are set to `UserTesting` which means that you will run a grin blockchain local to your computer.
- `run_test_miner` is set to `true` to mine coins. If you're interested in mining on floonet or mainnet check out [grin-miner](https://github.com/mimblewimble/grin-miner).

#### Download grin binaries

1. [grin](https://github.com/mimblewimble/grin/releases)
1. [grin-wallet](https://github.com/mimblewimble/grin-wallet/releases)

Extract grin and grin-wallet

#### Run

`./grin --usernet`

- `./chain_data` is responsible for housing the blockchain
- `grin-server.log` that will be the output of the grin process.


#### Open `/{{grin-dir}}/grin-server.toml`

change `run_test_miner` from `false` to `true` 

uncomment `test_miner_wallet_url`

edit `test_miner_wallet_url` port to `{{grin-wallet.toml}}.owner_api_listen_port` 

```
e.g.
#test miner wallet URL (burns if this doesn't exist)
test_miner_wallet_url = "http://127.0.0.1:3420"
```

#### Run

`./grin-wallet --usernet init`

Follow the prompts

- `./wallet_data` is responsible for housing wallet information
- `grin-wallet.log` will be the output of the grin wallet process
- `.api_secret` is responsible for encrypting traffic between the `grin` and `grin-wallet`
- `.owner_api_secret` is responsible for encrypting traffic between the `grin-wallet` owner api and other services.

#### Run

`./grin-wallet --usernet owner_api --run_foreign`

The `grin-wallet --usernet --run_foreign owner_api` command will start the api listener.



##### You can find documentation about the grin-wallet cli and rpc below:

- [Grin Official CLI documentation](https://github.com/mimblewimble/docs/wiki/Wallet-User-Guide)
- [Grin Official JSON RPC API documentation](https://github.com/mimblewimble/docs/wiki/Wallet-JSON-RPC-API-Guide)

# [Work Together](https://github.com/gringineer?tab=stars)
