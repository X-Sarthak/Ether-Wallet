## Ether-Wallet: ERC-20 Token Project

This project is a React.js-based Ethereum wallet that interacts with an ERC-20 token deployed using **Ether.js, Truffle, Ganache, Remix, and MetaMask**.

## Features
- Connect MetaMask to interact with Ethereum blockchain.
- Deploy and interact with an ERC-20 token.
- Send and receive tokens.
- Check wallet balance.
- Smart contract interactions using **ethers.js**.

---

## Technologies Used

- **Frontend**: React.js
- **Blockchain Interaction**: ethers.js
- **Smart Contract Development**: Solidity, Truffle, Remix
- **Local Blockchain Testing**: Ganache
- **Wallet Integration**: MetaMask

---

## Getting Started

### Prerequisites

Ensure you have the following installed:

- **Node.js** (v16+ recommended)
- **MetaMask Extension** (for interacting with the Ethereum blockchain)
- **Ganache** (for local blockchain development)
- **Truffle** (for compiling and deploying smart contracts)

Install Truffle globally:

```sh
npm install -g truffle
```

---

## Project Setup

1. **Clone the Repository**:

```sh
git clone https://github.com/your-repo/ether-wallet.git
cd ether-wallet
```

2. **Install Dependencies**:

```sh
npm install
```

3. **Run the Development Server**:

```sh
npm start
```

This will start the React application at `http://localhost:3000`.

---

## Deploying the ERC-20 Smart Contract

### 1. Setup Ganache

- Open Ganache and start a new workspace.
- Note the RPC server URL (e.g., `http://127.0.0.1:7545`).

### 2. Compile and Deploy Smart Contract

Navigate to the **Truffle project directory** and run:

```sh
truffle compile
truffle migrate --network development
```

This deploys the contract to your local Ganache blockchain.

---

## Connecting MetaMask to Ganache

1. Open MetaMask and select **Network > Add Network**.
2. Enter **RPC URL** from Ganache (`http://127.0.0.1:7545`).
3. Import an account using one of Ganache’s private keys.

---

## Interacting with the Smart Contract

### Importing the ERC-20 Token to MetaMask

1. Copy the **deployed contract address** from Truffle.
2. Open MetaMask, click **Import Tokens**, and paste the address.

### Sending Tokens

1. Use the React.js app to send tokens.
2. MetaMask will prompt for transaction confirmation.

---

---

## Smart Contract (ERC-20 Token)

Example ERC-20 Solidity contract:

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";

contract MyToken is ERC20 {
    constructor(uint256 initialSupply) ERC20("MyToken", "MTK") {
        _mint(msg.sender, initialSupply * (10 ** decimals()));
    }
}
```

---

## Build for Production

```sh
npm run build
```

---

## License

MIT License.

---
