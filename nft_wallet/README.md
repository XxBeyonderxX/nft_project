# NFT Wallet DApp

## Overview

This NFT wallet DApp serves as an example, utilizing minted NFTs from the Rust dip721-nft-container. Key features include NFT registration, transferring NFTs, and checking the NFT count. The DApp comes with a user-friendly frontend UI for seamless interaction.

## Prerequisites

Ensure the following installations:

- [x] [IC SDK](https://internetcomputer.org/docs/current/developer-docs/setup/install/index.mdx)

## Deployment

### Step 1: Deploy the DApp

Use the provided `start.sh` script for quick deployment:

```bash
./start.sh
```

Alternatively, deploy manually:

```bash
dfx start --background
cd internet-identity
npm install
II_FETCH_ROOT_KEY=1 dfx deploy
cd ..
./deploy.sh
```

### Step 2: Deploy on IC Network (Optional)

For IC network deployment:

```bash
./deploy.sh --network ic
```

### Step 3: Execute DApp Calls

Make calls to the NFT wallet canister. For instance, to transfer an NFT:

```bash
dfx canister call nftwallet transfer '(record {canister = principal "<NFT canister id>"; index = 1:nat64}, principal "<recipient canister id>", opt true)'
```

Adjust commands based on your specific use case.

Explore the NFT wallet DApp with ease!