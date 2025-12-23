# AstraDeFi Smart Contracts

This repository contains the Solidity smart contracts and subgraph configurations for the AstraDeFi platform. The contracts cover a wide range of DeFi functionalities, including staking, rewards, liquidity provision, automated market makers (AMM), and more. These contracts are deployed across multiple test networks to ensure broad coverage and scalability.

## Contracts Overview

The following key contracts are deployed across various networks:

- Staking Token Contract: Users can stake their tokens in this contract to participate in the platform.
- Reward Token Contract: Provides rewards to users who participate in staking or liquidity provision.
- Staking Contract: Manages staking, rewards, and other related functionalities.
- AMM Contract: Automated market maker contract for facilitating decentralized trading and liquidity.
- Faucet Contract: Provides tokens for testing purposes on supported networks.

### Supported Networks & Chain IDs

- ETH Sepolia Testnet (11155111)
- ETH Holesky Testnet (17000)
- Optimism Sepolia Testnet (11155420)
- Mode Testnet (919)
- Base Sepolia Testnet (84532)
- Polygon Amoy Testnet (80002)

Each network has its own set of contract addresses and subgraph URLs for data querying.

## Tech Stack

### Smart Contract Development:
- Solidity: Smart contracts are written using Solidity 0.8.24.
- OpenZeppelin: Standardized and secure contract modules (e.g., ERC20, Ownable) from OpenZeppelin.
- Hardhat: Development environment for compiling, testing, and deploying contracts.
- Hardhat Toolbox: Suite of plugins for debugging, testing, and verifying contracts.
- Hardhat Verify: Plugin to verify contracts on blockchain explorers.

### Graph Protocol:
- The Graph: Decentralized indexing protocol to query blockchain data.
- Graph CLI: For building and deploying subgraphs to track contract data.

## Multiple Chains & Contract Addresses

AstraDeFi contracts are deployed across multiple test networks to provide access to different blockchains. Here are the configurations for each chain:

### ETH Sepolia Testnet (Chain ID: 11155111)
- Staking Token Contract: 0x8fA88684F4233AbF617DE993bdFD3B4b0077626B
- Reward Token Contract: 0x4e7059F901c8D5e0636c5733559ed9a3440d2408
- Staking Contract: 0x5A67Fe909861a16937e84027657Cce21C1cC3a6a
- Faucet Contract: 0x5CfC46B79Aaf7771A2Ce335f825d61F5a4EAEEbe
- AMM Contract: 0x0Db6DA5FE73Aa80c82ccbC5C805f298718B5ed34

### ETH Holesky Testnet (Chain ID: 17000)
- Staking Token Contract: 0x09572c39b311834047b694EC77A614822ffBb1ff
- Reward Token Contract: 0xc0C357bCCc6CFfeef97b792c72774b4c47B3D884
- Staking Contract: 0x3B61C76fAD6c88FA565Ed538524d10C25f63ee75
- Faucet Contract: 0xBD22719907F3839EEc1f7482Af0788e26ed447F9
- AMM Contract: 0x21fb6F632054669EA240adAF0BCd6930Ba029A82

### Optimism Sepolia Testnet (Chain ID: 11155420)
- Staking Token Contract: 0xBD22719907F3839EEc1f7482Af0788e26ed447F9
- Reward Token Contract: 0x21fb6F632054669EA240adAF0BCd6930Ba029A82
- Staking Contract: 0x592bCA70afd3ef10c91bE4fc5c07Dcc7f1AC890d
- Faucet Contract: 0x17B50Cf3d0490C3290E8bBC0758C427B9Bf763e9
- AMM Contract: 0x533557766fBeC9825700A8Fbde88bf7B3A28dEBd

### Mode Testnet (Chain ID: 919)
- Staking Token Contract: 0x74df726F77387ebDA41b0b52056A862f41237C0d
- Reward Token Contract: 0x742Df2E9B29bA22687FC509f9356776176273DaB
- Staking Contract: 0xdfE84AAb2A3E9Db1b35A64Ccf05faB6bFfBb63b7
- Faucet Contract: 0xafA061A7127C0b1929FA9068413ccF1C9335a368
- AMM Contract: 0x669C5f1a698Ab3a56A1a85b64dCFFE5fE2bB7e1F

### Base Sepolia Testnet (Chain ID: 84532)
- Staking Token Contract: 0x09572c39b311834047b694EC77A614822ffBb1ff
- Reward Token Contract: 0xc0C357bCCc6CFfeef97b792c72774b4c47B3D884
- Staking Contract: 0x3B61C76fAD6c88FA565Ed538524d10C25f63ee75
- Faucet Contract: 0xBD22719907F3839EEc1f7482Af0788e26ed447F9
- AMM Contract: 0x21fb6F632054669EA240adAF0BCd6930Ba029A82

### Polygon Amoy Testnet (Chain ID: 80002)
- Staking Token Contract: 0x09572c39b311834047b694EC77A614822ffBb1ff
- Reward Token Contract: 0xc0C357bCCc6CFfeef97b792c72774b4c47B3D884
- Staking Contract: 0x3B61C76fAD6c88FA565Ed538524d10C25f63ee75
- Faucet Contract: 0xBD22719907F3839EEc1f7482Af0788e26ed447F9
- AMM Contract: 0x21fb6F632054669EA240adAF0BCd6930Ba029A82

## Development Setup

To get started with the development of the smart contracts and The Graph subgraphs:

### Step 1: Clone the Repository

```bash
git clone https://github.com/your-username/astradefi-contracts.git
cd astradefi-contracts
```

### Step 2: Install Dependencies

```bash
npm install
```

### Step 3: Set Up Environment Variables

Create a `.env` file in the root directory and add your private key:

```
SEPOLIA_PRIVATE_KEY=your_private_key_here
```

### Step 4: Compile Contracts

Compile the smart contracts using Hardhat:

```bash
npx hardhat compile
```

### Step 5: Deploy Contracts

To deploy the contracts to a specific network:

```bash
npx hardhat run scripts/deploy.ts --network <network-name>
```

Replace <network-name> with the target network (e.g., ethSepolia, polygonAmoyTestnet, etc.).

Alternatively, use Hardhat Ignition for deployment:

```bash
npx hardhat ignition deploy ./ignition/modules/Staking.ts --network <network-name>
```

### Step 6: Verify Contracts

To verify the contracts on the blockchain explorers:

```bash
npx hardhat verify --network <network-name> <contract-address>
```

### Step 7: Testing

To run tests:

```bash
npx hardhat test
```

To run tests with gas reporting:

```bash
REPORT_GAS=true npx hardhat test
```

## Project Structure

```
omni-contracts/
├── contracts/          # Solidity smart contracts
│   ├── AMM.sol         # Automated Market Maker contract
│   ├── Staking.sol     # Staking and rewards contract
│   ├── Faucet.sol      # Token faucet for testing
│   ├── RewardToken.sol # Reward token ERC20 contract
│   └── StakingToken.sol # Staking token ERC20 contract
├── test/               # Test files
│   ├── Staking.ts      # Staking contract tests
│   ├── Faucet.ts       # Faucet contract tests
│   └── Token.ts        # Token contract tests
├── scripts/            # Deployment scripts
│   └── deploy.ts       # Main deployment script
├── ignition/           # Hardhat Ignition modules
│   └── modules/        # Deployment modules
├── hardhat.config.ts   # Hardhat configuration
├── package.json        # Project dependencies
└── tsconfig.json       # TypeScript configuration
```

## Contract Features

### Staking Contract
- Stake tokens to earn rewards
- Withdraw staked tokens
- Claim earned rewards
- Take loans against staked tokens (up to 80% of staked amount)
- Repay loans with interest
- Pausable functionality for emergency situations
- Owner-controlled reward rate and interest rate

### AMM Contract
- Provide liquidity to token pairs
- Remove liquidity
- Swap tokens with slippage protection
- Calculate swap details before execution
- View current token prices
- Calculate required token amounts for liquidity provision

### Faucet Contract
- Claim tokens for testing
- Time-based claim intervals
- Owner-controlled claim amount and interval
- Owner can withdraw tokens

## Security Features

- ReentrancyGuard protection on all state-changing functions
- Ownable pattern for access control
- Pausable functionality for emergency stops
- Custom errors for gas-efficient error handling
- Input validation on all user-facing functions
- Slippage protection on swaps

## Gas Optimizations

- Custom errors instead of require strings
- Efficient storage variable packing
- Minimal external calls
- Optimized mathematical operations
- Use of immutable variables where possible

## Contribution Guidelines

We welcome contributions to improve AstraDeFi's smart contracts and subgraph. Please open an issue or submit a pull request with your proposed changes.

## License

This repository is licensed under the MIT License. See the LICENSE file for more details.

## Useful Hardhat Commands

```bash
npx hardhat help
npx hardhat test
REPORT_GAS=true npx hardhat test
npx hardhat node
npx hardhat compile
npx hardhat clean
```
