## Walk Through: Create Local Grin Development Enviroment

This walkthough will create an enviroment is useful if you want to develop with grin locally.

**Note:**

- `chain_type` in your `grin-wallet.toml` and `grin-node.toml` are set to `UserTesting` which means that you will run a grin blockchain local to your computer.
- `run_test_miner` is set to `true` to mine coins. If you're interested in mining on floonet or mainnet check out [grin-miner](https://github.com/mimblewimble/grin-miner).

#### Clone gringineer

`git clone https://github.com/gringineer/gringineer.git`

#### Download grin binaries

1. [grin](https://github.com/mimblewimble/grin/releases)
1. [grin-wallet](https://github.com/mimblewimble/grin-wallet/releases)

Extract grin and grin-wallet to gringineer

#### Open Terminal && Run

`./grin`

- `./chain_data` is responsible for housing the blockchain
- `grin-server.log` that will be the output of the grin process.

#### Open Terminal && Run

`./grin-wallet init`

Follow the prompts

- `./wallet_data` is responsible for housing wallet information
- `grin-wallet.log` will be the output of the grin wallet process
- `.api_secret` is responsible for encrypting traffic between the `grin` and `grin-wallet`
- `.owner_api_secret` is responsible for encrypting traffic between the `grin-wallet` owner api and other services.

After

`./grin-wallet listen`

The `grin-wallet listen` command will start the owner api listener and allow your to receive your `UserTesting` coins that your grin process will mine.

##### You can find documentation about the grin-wallet cli and rpc below:

- [Grin Official CLI documentation](https://github.com/mimblewimble/docs/wiki/Wallet-User-Guide)
- [Grin Official JSON RPC API documentation](https://github.com/mimblewimble/docs/wiki/Wallet-JSON-RPC-API-Guide)

Have other questions?
[Get In Touch](https://keybase.io/gringineer)
