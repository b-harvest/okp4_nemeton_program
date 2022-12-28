# OKP4 Monitoring

A popular monitoring tool for Tendermint based chains like OKP4 is [Tenderduty](https://github.com/blockpane/tenderduty).

![dashboard screenshot](https://github.com/blockpane/tenderduty/blob/main/docs/dash.png?raw=true)

To get started, follow below steps:

1. Refer to the [official installation doc](https://github.com/blockpane/tenderduty/blob/main/docs/install.md) and install tenderduty.

2. Make [config.yml](config.yml) file in your tenderduty working directory.

3. Edit `config.yml` based on your preferences:

   - Set listening port
   - Get API keys (Discord, Telegram, PagerDuty) and set your alert config
   - etc.

4. Make `chains.d` directory.

5. Make [okp4.yml](okp4.yml) file in `chains.d` directory.
   In this case `okp4` will be label.
   You can make file what you want to been label like `<monitoring label>.yml`.

6. Edit `okp4.yml` based on your validator and preferences:

   - Add chain ID (`okp4-nemeton-1` for Nemeton Program)
   - Add your valoper address (using `okp4d keys show <keyname> -a --bech val`)
   - Add RPC endpoints (must be `protocol://hostname:port`)
   - etc.

7. Start service and access service page (e.g. `http://localhost:8888`)
