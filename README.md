# Dappcord - Decentralized Discord DApp

**A blockchain-powered decentralized communication platform inspired by Discord, where users pay ETH to mint NFT membership tokens for accessing exclusive channels.**

This project demonstrates a full-stack decentralized application (DApp) combining **Solidity smart contracts** for on-chain logic (channel creation, NFT minting for access control, and fund withdrawal) with a **React.js** frontend for user interaction and **Socket.io** for real-time messaging.

The core focus is on robust smart contract development: writing secure, tested Solidity code using modern best practices, comprehensive unit testing, and local deployment with Hardhat.

![Project Architecture Diagram](IMG_0909.jpeg)

## Key Features

- **Smart Contract Functionality**:
  - Create new channels on-chain.
  - Mint ERC-721 NFT membership tokens by paying a set amount of ETH (access control via ownership).
  - Owner can withdraw accumulated ETH from mints.
  - Events emitted for real-time frontend updates.

- **Frontend**:
  - Wallet connection (MetaMask).
  - Display channels and membership status.
  - Mint NFT to join paid channels.
  - Real-time chat using Socket.io (off-chain for performance).

- **Real-time Communication**:
  - Socket.io server handles live messaging within channels.

![App Screenshot](ss.png)

## Technology Stack & Tools

- **Solidity** → Writing Smart Contracts & Comprehensive Tests
- **Hardhat** → Development Framework (Compilation, Testing, Deployment, Local Network)
- **Ethers.js** → Blockchain Interaction & Wallet Integration
- **React.js** → Frontend Framework
- **Socket.io** → Real-time Client-Server Communication
- **Node.js** → Backend Server for Socket.io

## Smart Contract Highlights

The `Dappcord.sol` contract is fully implemented with:
- Channel management (create channels with name and cost).
- ERC-721 NFT minting (unique token ID per membership, cost in ETH).
- Access control (only NFT owners can join channels).
- Secure owner-only withdrawal.
- Events for channel creation and minting.

**Extensive testing** using Hardhat and Chai:
- Covers channel creation, minting, access restrictions, withdrawal, and edge cases.
- Run with `npx hardhat test` → All tests passing.
