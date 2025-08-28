# Beacon Proxy

## Deploy

```bash
cargo stylus deploy \
  -e=$RPC_URL \
  --private-key=$PRIV_KEY \
  --wasm-file=$WASM_FILE \
  --no-verify \
  --deployer-address=$DEPLOYER_ADDRESS \
  --constructor-signature 'constructor(address,bytes)' \
  --constructor-args <UPGRADEABLE_BEACON_ADDRESS> <DATA>
```

## Get Implementation Address

```bash
cast call <CONTRACT_ADDRESS> "implementation()(address)" --rpc-url $RPC_URL
```

## Get Upgradeable Beacon Address

```bash
 cast call <CONTRACT_ADDRESS> "getBeacon()(address)" --rpc-url $RPC_URL
```
