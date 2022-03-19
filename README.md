# Asset Parachain💲💲💲💲💲💲:running:
> For Studying the XCM in polkadot

### This is an Asset Parachain connected to the rococo test network


## start Asset chain
```
 ./target/release/parachain-Asset build-spec --disable-default-bootnode > rococo-local-parachain-plain.json 

./target/release/parachain-Asset build-spec --chain rococo-local-parachain-plain.json --raw --disable-default-bootnode > rococo-local-parachain-4000-raw.json

 ./target/release/parachain-Asset export-genesis-wasm --chain rococo-local-parachain-4000-raw.json > para-4000-wasm

./target/release/parachain-Asset  export-genesis-state --chain rococo-local-parachain-4000-raw.json > para-4000-genesis

 ./target/release/parachain-Asset \
--bob \
--collator \
--force-authoring \
--chain rococo-local-parachain-4000-raw.json \
--base-path /tmp/parachain/bob \
--port 40334 \
--ws-port 8855 \
-- \
--execution wasm \
--chain ../../polkadot-0.9.16/rococo-local-cfde.json \ 
--port 30344 \
--ws-port 9988
```