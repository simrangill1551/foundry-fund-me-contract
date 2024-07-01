# FundMe Smart Contract

## Overview

The `FundMe` smart contract allows users to contribute funds to a pool and provides mechanisms for the owner to withdraw these funds. This contract uses Chainlink oracles to fetch the latest ETH/USD price to ensure that all contributions meet a minimum USD value.

## Features
- **Fund**: Allows users to contribute funds.
- **Withdraw**: Allows the owner to withdraw all funds.
- **Cheaper Withdraw**: A more gas-efficient withdrawal method for the owner.
- **Price Feed Integration**: Uses Chainlink to get the latest ETH/USD price.

## Prerequisites
- Solidity `^0.8.2`
- Chainlink AggregatorV3Interface
- PriceConverter library

## Installation
1. **Clone the repository**:
    ```sh
    git clone https://github.com/repo/FundMe.git
    cd FundMe
    ```

2. **Install dependencies**:
    Ensure you have the required dependencies installed, such as OpenZeppelin for the `AggregatorV3Interface`.

3. **Compile the contract**:
    Use your preferred Solidity compiler to compile the `FundMe.sol` contract.

## Usage
1. **Deploy the contract**:
    Deploy the `FundMe` contract, providing the address of the Chainlink price feed as a parameter.

2. **Fund the contract**:
    Call the `fund` function and send ETH. The contract checks if the sent ETH value is equivalent to or above the minimum USD value.

3. **Withdraw funds**:
    Only the contract owner can call the `withdraw` or `cheaperWithdraw` functions to withdraw the accumulated funds.
