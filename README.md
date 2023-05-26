# KaseiCoin Crowdsale Project

This project involves creating a decentralized crowdfunding mechanism using smart contracts on a local blockchain. The project includes the creation of the KaseiCoin token contract, the KaseiCoin crowdsale contract, and the KaseiCoin deployer contract. 

## Instructions

### Step 1: Create the KaseiCoin Token Contract

1. Import the provided `KaseiCoin.sol` starter file into the Remix IDE.
2. Import the following contracts from the OpenZeppelin library:
   - ERC20
   - ERC20Detailed
   - ERC20Mintable
3. Define a contract for the KaseiCoin token named `KaseiCoin` and inherit the three imported contracts from OpenZeppelin.
4. Add a constructor to the KaseiCoin contract with parameters for `name`, `symbol`, and `initial_supply`.
5. In the constructor, call the constructor of the ERC20Detailed contract, passing the appropriate parameters.
6. Compile the contract using version 0.5.5 of the compiler.

### Step 2: Create the KaseiCoin Crowdsale Contract

1. Import the provided `KaseiCoinCrowdsale.sol` starter code into the Remix IDE.
2. Inherit the following OpenZeppelin contracts in the KaseiCoinCrowdsale contract:
   - Crowdsale
   - MintedCrowdsale
3. Define the KaseiCoinCrowdsale constructor with parameters for rate, wallet, and token. Configure these parameters based on your KaseiCoin token specifications.
4. Compile the contract using version 0.5.5 of the compiler.

### Step 3: Create the KaseiCoin Deployer Contract

1. Uncomment the KaseiCoinCrowdsaleDeployer contract in the provided `KaseiCoinCrowdsale.sol` starter code.
2. Add variables in the KaseiCoinCrowdsaleDeployer contract to store the addresses of the KaseiCoin and KaseiCoinCrowdsale contracts that will be deployed.
3. Create public address variables, `kasei_token_address` and `kasei_crowdsale_address`, to store the respective contract addresses once deployed.
4. Add parameters to the constructor of the KaseiCoinCrowdsaleDeployer contract: name, symbol, and wallet.
5. Inside the constructor, create the KaseiCoin token instance and assign its address to the `kasei_token_address` variable.
6. Create a new instance of the KaseiCoinCrowdsale contract with the provided parameters and assign its address to the `kasei_crowdsale_address` variable.
7. Set the KaseiCoinCrowdsale contract as a minter and renounce the minter role for the KaseiCoinCrowdsaleDeployer contract.
8. Compile the contract using version 0.5.5 of the compiler.

