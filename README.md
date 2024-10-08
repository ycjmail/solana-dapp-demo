# solana-dapp-demo

```
npx create-solana-dapp@latest 
```
The project name is solana-dapp-demo,and the others are default

## Getting Started

### Prerequisites

- Node v18.18.0 or higher

- Rust v1.77.2 or higher
- Anchor CLI 0.30.0 or higher
- Solana CLI 1.18.9 or higher

### Installation

#### Install Dependencies

```shell
pnpm install
```

#### Start the web app

```
pnpm run dev
```

## Apps

### anchor

This is a Solana program written in Rust using the Anchor framework.

#### Commands

You can use any normal anchor commands. Either move to the `anchor` directory and run the `anchor` command or prefix the command with `npm run`, eg: `npm run anchor`.

#### Sync the program id:

Running this command will create a new keypair in the `anchor/target/deploy` directory and save the address to the Anchor config file and update the `declare_id!` macro in the `./src/lib.rs` file of the program.

You will manually need to update the constant in `anchor/lib/counter-exports.ts` to match the new program id.

```shell
npm run anchor keys sync
```

#### Build the program:

```shell
npm run anchor-build
```

#### Start the test validator with the program deployed:

```shell
npm run anchor-localnet
```

#### Run the tests

```shell
npm run anchor-test
```

#### Deploy to Devnet

```shell
npm run anchor deploy --provider.cluster devnet
```

### web

This is a React app that uses the Anchor generated client to interact with the Solana program.

#### Commands

Start the web app

```shell
npm run dev
```

Build the web app

```shell
npm run build
```



#### Deploy to localnet


```shell
solana-test-validator
```

```shell
cd anchor
avm use 0.30.0
anchor keys sync
anchor build
anchor deploy
cd ..
```

### web

This is a React app that uses the Anchor generated client to interact with the Solana program.

#### Commands

Start the web app

```shell
npm run dev
```

To visit http://localhost:3000/ using a web browser.

test on localnet screenshot

![solana-dapp-demo](solana-dapp-demo.jpg )


