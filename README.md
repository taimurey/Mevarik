# Mevarik Sniper (Beta Version)

This guide will walk you through the process of deploying and running the Mevarik Sniper. It will also explain the various settings in the `Settings.json` file.

## Deployment

1. Download the release file using the `wget` command. Replace `<Link to Release File>` with the actual link to the release file.

    ```bash
    wget <Link to Release File>
    ```

## Execution

1. Make the downloaded file executable using the `chmod` command.

    ```bash
    sudo chmod +x Mevarik
    ```

2. Run the executable file.

    ```bash
    ./Mevarik
    ```

## Settings Explanation

The `Settings.json` file contains various settings that control the behavior of the Mevarik Sniper. Here is an explanation of each setting:

- `pubsub_url`: The URL of the PubSub server. This is where the Mevarik Sniper will subscribe to receive updates.
- `rpc_url`: The URL of the RPC server. This is where the Mevarik Sniper will send RPC requests.
- `block_engine_url`: The URL of the BlockEngine server. This is where the Mevarik Sniper will get block data.
- `message`: The message that will be sent with each tip.
- `grpc_url`: The URL of the gRPC server. This is where the Mevarik Sniper will send gRPC requests.
- `buy_wallet`: The private key of the wallet that will be used to buy tips.
- `bot:auth`: The private key of the whitelisted address that the bot will use for authentication.
- `regions`: An array of regions where the Mevarik Sniper will operate.
- `subscribe_bundle_results`: A boolean value that determines whether the Mevarik Sniper will subscribe to bundle results.
- `use_bundles`: A boolean value that determines whether the Mevarik Sniper will use bundles.


## Settings.json

Settings.json
```bash
{
    "pubsub_url": "wss://mainnet.helius-rpc.com",
    "rpc_url": "https://mainnet.helius-rpc.com/",
    "block_engine_url": "https://ny.mainnet.block-engine.jito.wtf",
    "message": "Jito Tip Message",
    "grpc_url": "http://205.209.109.10:10000/",
    "buy_wallet": "<WALLET-PRIVATE-KEY>",
    "bot:auth": "<PRIVATE-KEY-OF-WHITELISTED-ADDRESS>",
    "regions": [
        "ny"
    ],
    "subscribe_bundle_results": false,
    "use_bundles": true
}
```