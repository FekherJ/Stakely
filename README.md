
# Staking and Yield Farming Smart Contract

This project demonstrates a **staking and yield farming contract** written in Solidity. Users can stake ERC-20 tokens and earn rewards over time, with features for withdrawing stakes and claiming rewards.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation and Setup](#installation-and-setup)
- [Usage](#usage)
- [Testing](#testing)
- [Deployment](#deployment)
- [Front-End Integration](#front-end-integration)
- [License](#license)

## Introduction

The **Staking and Yield Farming Contract** allows users to:
- Stake ERC-20 tokens.
- Earn rewards based on how long they have staked their tokens.
- Withdraw their staked tokens at any time.
- Claim rewards once they have been earned.

This contract is intended to provide a simple mechanism for staking, with future plans for implementing yield farming and more advanced reward mechanisms.

## Features

- **Staking**: Users can stake an amount of ERC-20 tokens in exchange for rewards.
- **Rewards**: Rewards are distributed based on a predefined reward rate.
- **Withdrawals**: Users can withdraw their staked tokens at any time.
- **Claim Rewards**: Users can claim accumulated rewards from staking.
- **Event Emissions**: Contract emits events for staking, withdrawal, and reward claims.

## Technologies Used

- **Solidity**: Smart contract language for writing the staking logic.
- **Hardhat**: Ethereum development environment.
- **OpenZeppelin**: Library for using standard ERC-20 token interfaces.
- **Ethers.js**: JavaScript library for interacting with the Ethereum blockchain (optional for front-end).
- **Node.js**: For managing dependencies and running the development environment.

## Installation and Setup

To get started with this project, follow these steps:

### Prerequisites

Ensure you have the following installed:
- **Node.js** (https://nodejs.org/)
- **npm** or **yarn**

### Install Dependencies

1. Clone the repository:
   ```bash
   git clone https://github.com/FekherJ/Stakely.git
   cd staking-contract
   ```

2. Install the project dependencies:
   ```bash
   npm install
   ```

3. Install **OpenZeppelin** contracts:
   ```bash
   npm install @openzeppelin/contracts
   ```

### Hardhat Setup

1. Create a new Hardhat project:
   ```bash
   npx hardhat
   ```

2. Follow the prompts to create a basic project structure.

### Configuration

In your `hardhat.config.js`, set up the required network details (for testnets or mainnet deployment) by adding Infura/Alchemy and your private key for deployment.

## Usage

### Staking Tokens

1. Deploy the contract using Hardhat.
2. Users can stake ERC-20 tokens by interacting with the `stake` function.
3. Staked tokens will accumulate rewards based on the `rewardRate`.

### Withdrawing Tokens

1. Users can withdraw their staked tokens by calling the `withdraw` function.
2. The contract ensures that users cannot withdraw more than they have staked.

### Claiming Rewards

1. Users can call the `getReward` function to claim their earned rewards.

## Testing

- You can test the contract using **Hardhat**. Write tests to verify:
  - Users can stake tokens.
  - Rewards are calculated correctly over time.
  - Users can withdraw staked tokens.
  - Users can claim rewards.
  
Run the tests with:
```bash
npx hardhat test
```

## Deployment

You can deploy the contract to a testnet (like Goerli) or mainnet using Hardhat.

1. Update your `hardhat.config.js` with the testnet or mainnet configuration (Infura/Alchemy keys, private key).
2. Deploy the contract using:
```bash
npx hardhat run scripts/deploy.js --network goerli
```

## Front-End Integration

- You can integrate this smart contract with a front-end dApp using **React** and **ethers.js**.
- Create a dashboard to show:
  - User staked balances.
  - Earned rewards.
  - Withdraw and claim buttons.

## License

This project is licensed under the MIT License.
