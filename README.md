# Contracts

```bash
export ECO=$(<./neardev/dev-account)
export USER1=kaito021201.testnet \ jewel goose vibrant minimum exhaust feature crystal solar any toe hire novel
export USER2=kaito021202.testnet \ vapor coast fossil call acquire sadness pole scare ahead jump dignity zebra
```

## Deploy Fungible Token


```bash
cd ft_token
cargo make clean
cargo make build
cargo make dev-deploy
 
cargo make call new_default_meta '{"owner_id": "'$ECO'", "total_supply": "1000000000"}' --accountId $ECO

cargo make call storage_deposit '' --accountId $USER1 --amount 0.00125

cargo make call ft_transfer '{"receiver_id": "'$USER1'", "amount": "100"}' --accountId $ECO --amount 0.000000000000000000000001

near view $ECO ft_balance_of '{"account_id": "'$USER1'"}

```


## Deploy Faucet


