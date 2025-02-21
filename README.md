# EngageRewards

## Project Description

EngageMint Token is a Solidity-based smart contract that mints tokens for users who engage with the platform. The purpose of this project is to incentivize user interaction by rewarding them with tokens that can be used within the platform.

## Smart Contract Address

The deployed smart contract can be found at the following address:

```
0x84D62C88B3229Ee9A72daC56A6fc0f0e14d56720
```

## Overview

This project includes the following features:

- Minting tokens for user engagement
- Transferring tokens between users
- Approving and transferring tokens on behalf of other users

## Smart Contract

The smart contract `EngageMintToken` is written in Solidity and includes the following functionalities:

- `mint(address _to, uint256 _amount)`: Mints new tokens to the specified address.
- `transfer(address _to, uint256 _value)`: Transfers tokens from the sender to the specified address.
- `approve(address _spender, uint256 _value)`: Approves the specified address to spend a certain amount of tokens on behalf of the sender.
- `transferFrom(address _from, address _to, uint256 _value)`: Transfers tokens from one address to another, provided the sender has been approved to do so.

## Getting Started

To get started with this project, follow these steps:

### Prerequisites

- Node.js and npm installed
- Solidity compiler (solc)
- Hardhat

### Installation

1. Clone the repository:

```bash
git clone https://github.com/jainhardik06/engagemint-token.git
cd engagemint-token
```

2. Install dependencies:

```bash
npm install
```

### Compilation

Compile the smart contract using Hardhat:

```bash
npx hardhat compile
```

### Deployment

Deploy the smart contract to a local blockchain (Hardhat Network):

```bash
npx hardhat run scripts/deploy.js --network localhost
```

### Interacting with the Smart Contract

Open the Hardhat console:

```bash
npx hardhat console --network localhost
```

Interact with the deployed smart contract:

```javascript
const EngageMintToken = await ethers.getContractFactory("EngageMintToken");
const token = await EngageMintToken.attach("0x84D62C88B3229Ee9A72daC56A6fc0f0e14d56720");

await token.mint("0xYourAddress", ethers.utils.parseUnits("100", 18));
let balance = await token.balanceOf("0xYourAddress");
console.log("Balance:", ethers.utils.formatUnits(balance, 18));
```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Inspiration for this project was drawn from various token-based incentive models.
- Thanks to the Ethereum community for providing extensive resources on smart contract development.
