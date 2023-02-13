## MDI TOKEN - Introduction

MDI token was issued in reference to DIP20 and is used as the reference currency for ICP-based medical projects.
Please refer to the white paper for the details of token economy, which was conducted using only motoko code in DIP20.

[https://www.medicle.io/_files/ugd/0a74e1_09b21d6bcb904262a08100270b6390b1.pdf]

## Development

You need the latest DFINITY Canister SDK to be able to build and deploy a token canister:

```shell
sh -ci "$(curl -fsSL https://sdk.dfinity.org/install.sh)"
```

Navigate to a the sub directory and start a local development network:

```shell
cd motoko
dfx start --background
```

Create canisters:

```shell
dfx canister create --all
```

Install code for token canister:

```
dfx build

dfx canister install token --argument="(\"<LOGO>\", \"<NAME>\", \"<SYMBOL>\", <DECIMALS>, <TOTAL_SUPPLY>, <YOUR_PRINCIPAL_ID>, <FEE>)"
e.g.:
dfx canister install token --argument="(\"data:image/jpeg;base64,...\", \"MDI\", \"MDI\", 8, 100000000000000000, principal \"aaa-bbb-ccc-dd\", 10000)"
```

Refer to `demo.sh` in the corresponding sub directory for more details.
