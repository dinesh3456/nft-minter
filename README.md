# NFT Minter

A Solana-based tool for creating NFT collections and minting NFTs on Devnet.

## Overview

This project provides scripts for:
- Creating NFT collections
- Minting NFTs that belong to a collection
- Verifying NFTs as part of a collection

All operations are performed on the Solana Devnet.

## Prerequisites

- Node.js and npm installed
- Basic understanding of Solana and NFTs
- Solana CLI tools (for key management)

## Installation

```bash
# Clone the repository
git clone https://github.com/dinesh3456/nft-minter.git
cd nft-minter

# Install dependencies
npm install
```

## Setup

This project requires a Solana keypair. Make sure you have a keypair file accessible to the scripts. The keypair is loaded using the `getKeypairFromFile()` function.

## Usage

### Creating an NFT Collection

Run the following command to create a new NFT collection:

```bash
npx esrun create-collection.ts
```

This will:
1. Load your keypair
2. Airdrop SOL if your balance is low
3. Create a collection NFT with name "My Collection"
4. Output the address of the collection NFT

### Creating an NFT

To create an NFT that belongs to a collection:

```bash
npx esrun create-nft.ts
```

This will:
1. Create a new NFT with name "My NFT"
2. Associate it with the collection (unverified)
3. Output the address of the created NFT

Note: You need to update the collection address in the script to match your collection.

### Verifying an NFT in a Collection

After creating an NFT, you can verify it as part of a collection:

```bash
npx esrun verify-nft.ts
```

This verifies that an NFT belongs to a specific collection.

Note: Update the NFT address and collection address in the script before running.

## Project Structure

- `create-collection.ts`: Script to create a new NFT collection
- `create-nft.ts`: Script to create an NFT associated with a collection
- `verify-nft.ts`: Script to verify an NFT as part of a collection

## Dependencies

- `@metaplex-foundation/mpl-token-metadata`: For NFT metadata operations
- `@metaplex-foundation/umi` and related packages: Metaplex Unified Metadata Interface
- `@solana-developers/helpers`: Helper functions for Solana development
- `esrun`: For running TypeScript files directly

## License

ISC
