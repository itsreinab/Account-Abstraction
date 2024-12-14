# Account Abstraction with ERC-4337

## Overview
This project implements **Account Abstraction** using the **ERC-4337** standard, enabling flexible, gas-efficient wallet management on the Ethereum blockchain. The core of this implementation revolves around custom smart wallets, entry point contracts, and bundlers for aggregating transactions, allowing for gasless interactions and advanced wallet functionalities.

The project demonstrates the process of building a fully decentralized account abstraction system with a focus on security, scalability, and gas optimization.

## Features
- **ERC-4337 Account Abstraction**: Custom user operations and entry point contracts.
- **Gasless Transactions**: Integration with **paymasters** to sponsor transaction fees.
- **Custom Wallet Architecture**: Supports multi-sig and social recovery schemes.
- **Gas Optimization**: Advanced gas cost minimization for smart wallet transactions.
- **Security**: Implements advanced security checks and defenses against common vulnerabilities.
- **Fuzz Testing**: Built-in testing framework using Foundry for real-world edge case simulations.

## Technologies Used
- **Solidity**: Ethereum smart contract development.
- **ERC-4337**: The standard for account abstraction.
- **Foundry**: A fast and secure framework for Ethereum development, used for testing and debugging.
- **Hardhat**: (if you used it in addition to Foundry) for deployment and script execution.
- **Ethereum**: Deployed on the Ethereum testnets (Rinkeby, Goerli, etc.).
- **MetaMask / Custom Wallet**: For interacting with custom wallets.
- **Gas Tokens / Paymasters**: For handling gasless transactions.

## Installation & Setup

### Prerequisites
1. **Node.js** (v14.x or higher)
2. **Foundry**: If not installed, run:
   ```bash
   curl -L https://foundry.paradigm.xyz | bash
   ```
3. **Hardhat** (optional) for deployment scripts:
   ```bash
   yarn add --dev hardhat
   ```

### Clone the Repository
To clone the repository, run the following command in your terminal:
```bash
git clone https://github.com/YOUR_USERNAME/Account-Abstraction-ERC4337.git
cd Account-Abstraction-ERC4337
```

### Install Dependencies
Run the following command to install the required dependencies:
```bash
yarn install
```

### Deploy Contracts
Deploy contracts using Foundry or Hardhat to your desired testnet. Follow the setup instructions in the Deploy Contracts section of the course.

### Run Tests
Run tests using Foundry's built-in testing framework:
```bash
forge test
```

## How It Works
1. **Account Abstraction**: ERC-4337 abstracts transaction handling, allowing users to initiate custom operations and use off-chain paymasters for gas payments.
2. **Entry Point Contract**: This contract acts as a central hub to validate and process user operations. It ensures that the user's custom operations are properly handled and validated.
3. **Gas Optimization**: Smart contract code is optimized for minimal gas usage by batching operations and leveraging efficient data structures.
4. **Paymaster Integration**: Paymasters sponsor transaction fees on behalf of users, enabling gasless interactions.
5. **Security Features**: The system includes robust defenses against replay attacks and other common vulnerabilities.

## Usage

### Interacting with the Wallet
1. **Deploy** your custom wallet using the provided contract templates.
2. **Submit User Operations**: Once the wallet is deployed, users can interact with it by submitting operations like token transfers or dApp interactions.
3. **Gasless Transactions**: The wallet allows users to send transactions without paying gas fees, as a paymaster sponsors the transaction.

## Testing & Validation
- The project includes comprehensive tests using Foundry to validate the implementation of account abstraction and gas optimizations.
- **Fuzz Testing**: Edge cases are simulated to ensure contract robustness.
- **Transaction Testing**: Ensures that user operations and wallet interactions are secure and efficient.

## Security Considerations
- **Replay Attack Prevention**: Ensures transactions cannot be reused maliciously.
- **Gas Fee Safeguards**: Protects users from excessive gas consumption.
- **Access Control**: Limits operations to authorized users, ensuring the integrity of wallet management.

## Contributing
1. Fork the repository.
2. Clone your fork:
   ```bash
   git clone https://github.com/YOUR_USERNAME/Account-Abstraction-ERC4337.git
   ```
3. Create a new branch:
   ```bash
   git checkout -b feature/your-feature
   ```
4. Commit your changes:
   ```bash
   git commit -m "Add feature"
   ```
5. Push to the branch:
   ```bash
   git push origin feature/your-feature
   ```
6. Create a Pull Request.

## License
Distributed under the MIT License. See LICENSE for more information.

## Acknowledgments
- Special thanks to **Cyfrin Updraft** for providing the course material and project structure that helped shape this implementation.
- Thanks to the **Ethereum** and **Foundry** communities for their tools and contributions.


