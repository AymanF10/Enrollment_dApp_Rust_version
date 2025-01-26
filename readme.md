# Turbine Prerequisite Program

## Overview

The **Turbine Prerequisite Program** is a Rust-based library for interacting with the Solana blockchain. It provides functionality for generating wallets, transferring SOL tokens, airdropping tokens, and enrolling users with associated GitHub accounts. This library is designed to be used with the Solana Devnet.

## Features

- Generate new Solana wallets.
- Convert wallet keys between formats (byte array and Base58).
- Airdrop SOL tokens to a wallet.
- Transfer SOL tokens between wallets.
- Enroll users by associating their GitHub accounts with a Solana program.

## Getting Started

### Prerequisites

- Rust (1.54 or higher)
- Cargo (comes with Rust)
- Solana CLI installed
- Access to the Solana Devnet

### Installation

1. Clone the repository:

   ```
   git clone <your-repo-url>
   cd <your-repo-directory>
   ```

2. Ensure you have the required dependencies in your `Cargo.toml` file. You can add the following dependencies:

   ```
   [dependencies]
   solana-client = "X.Y.Z"  # Replace with the latest version
   solana-program = "X.Y.Z"  # Replace with the latest version
   solana-sdk = "X.Y.Z"      # Replace with the latest version
   bs58 = "0.4"               # For Base58 encoding/decoding
   ```

3. Build the project:

   ```
   cargo build
   ```

### Usage

#### Generating a Wallet

To generate a new Solana wallet, run the following test function:

```
cargo test keygen
```

This will output your new wallet's public key and provide instructions on how to save it.

#### Airdropping SOL Tokens

To request an airdrop of SOL tokens to your wallet, ensure you have your wallet's keypair saved as `dev-wallet.json`, then run:

```
cargo test airdrop
```

#### Transferring SOL Tokens

To transfer SOL tokens from one wallet to another, ensure you have your wallet's keypair saved as `dev-wallet.json`, and specify the recipient's public key in the `transfer_sol` test function:

```
cargo test transfer_sol
```
#### Enrolling Users

To enroll a user by associating their GitHub account, ensure you have your wallet's keypair saved as `Turbin3-wallet.json`, then run:

```
cargo test enroll
```

### Running Tests

You can run all tests to verify functionality:

```
cargo test
```

## Contributing

Contributions are welcome! If you have suggestions or improvements, please create an issue or submit a pull request.

### License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

