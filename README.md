# Anchor-swap

This project aims to  build and deploy a simple AMM on Solana Network that used Anchor as a develop tool. This also refers to  [token-swap example](https://github.com/solana-labs/solana-program-library/tree/master/token-swap) and [anchor-amm](https://github.com/ironaddicteddog/anchor-amm)

## Build, Deploy and Test

First, install dependencies:

```
$ yarn
```

Next, we will build and deploy the program via Anchor.

Get the program ID:

```
$ anchor keys list
anchor_amm: 4CkSf34hTH2rGmgFDCm5WCFE8sHpfdBzrBChEScJBxoM
```

Here, make sure you update your program ID in `Anchor.toml` and `lib.rs`.

Build the program:

```
$ anchor build
```

Let's deploy the program. Notice that `anchor-amm` will be deployed on a [mainnet-fork](https://github.com/DappioWonderland/solana) test validator run by Dappio:

```
$ anchor deploy
...

Program Id: CEK6nMrUhNjUT2ki9eVskzwWRGLYdKTs7p77uNb5hVZt

Deploy success
```

Finally, run the test:

```
$ anchor test --skip-build --skip-deploy
```v

