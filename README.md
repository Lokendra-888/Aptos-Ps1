# Aptos Snap

A MetaMask Snap that lets you use Aptos accounts inside MetaMask, plus a small web app to try it. It can show addresses and keys, sign messages, and send APT on **Aptos Testnet**.

> Prototype for testnet only. Use throwaway accounts, never real funds.

## Requirements

- Node.js 24 (`nvm install && nvm use`)
- Yarn (`corepack enable`)
- [MetaMask Flask](https://metamask.io/flask/) (the developer build of MetaMask). Use a fresh profile with regular MetaMask disabled.

## How to use

```bash
git clone https://github.com/Lokendra-888/Aptos-Ps1.git
cd Aptos-Ps1
yarn install
yarn start
```

1. Open http://localhost:8000 in the browser with MetaMask Flask.
2. Click **Connect** and approve the snap in MetaMask.
3. Pick an account from the dropdown and use the buttons:
   - **Get AccountAddress / PublicKey / PrivateKey**: show the active account's details.
   - **Send Message**: sign a text message.
   - **Send Txn**: enter a receiver address and amount (in octas, 1 APT = 100,000,000), then approve in MetaMask. The account is auto-funded from the testnet faucet first.
   - **Create New Acc**: derive another account.
   - **Encrypt & Save Data**: store, read or clear key/value data in the snap.

After changing snap code, click **Reconnect** to reload it. Results appear in MetaMask dialogs and the browser console.

## Project structure

- `packages/snap`: the MetaMask Snap (runs on port 8080)
- `packages/site`: the test web app (runs on port 8000)

## Commands

```bash
yarn start   # run snap + web app
yarn build   # production build
yarn lint    # lint checks
```

## License

MIT-0 or Apache-2.0

This project is licensed under the [Apache 2.0 License](./LICENSE.APACHE2) and [MIT License](./LICENSE.MIT0).
