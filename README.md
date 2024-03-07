# Belt Subscription Smart Contract

This Solidity smart contract, named BeltSubscription, is designed to manage a subscription system where users can redeem different types of belts using a custom ERC20 token called BeltCoin (BELT). Each belt type has a different cost associated with it, and users can redeem a belt of their choice by spending the required amount of BeltCoin.

## Features

- **ERC20 Token**: The contract extends the ERC20 standard, allowing it to mint, burn, and transfer BeltCoin tokens.
- **Subscription System**: Users can redeem different types of belts (Leather, Fabric, Chain) by spending the required amount of BeltCoin tokens.
- **Ownership Control**: The contract inherits from Ownable.sol, ensuring that only the owner (deployer) has certain privileges like minting tokens.
- **Events**: Events are emitted for belt redemptions and token burns, providing transparency and allowing external systems to react to these actions.
- **Mapping**: User subscriptions (belt types) are stored in a mapping for easy retrieval.

## Contract Overview

- **Constructor**: Initializes the BeltCoin token with the name "BeltCoin" and symbol "BELT".
- **Mint Tokens**: Function `mintTokens` allows the owner to mint BeltCoin tokens and distribute them to specific addresses.
- **Burn Tokens**: Users can burn their BeltCoin tokens using the `burnTokens` function, reducing their balance.
- **Redeem Belt**: Users can redeem a belt of their choice by calling the `redeemBelt` function with the appropriate belt type number.
- **Transfer Tokens**: Function `transferTokens` allows users to transfer BeltCoin tokens to other addresses.
- **Get Belt Type**: Function `getBeltType` returns the type of belt associated with the caller's address.

## Usage

1. Deploy the contract to a supported Ethereum network (e.g., Rinkeby, Mainnet).
2. Mint BeltCoin tokens to the desired addresses using the `mintTokens` function.
3. Users can interact with the contract to redeem belts, burn tokens, transfer tokens, and query their belt type.

## Security Considerations

- **Ownership**: Ensure that the owner address is secure and controlled to prevent unauthorized access to minting privileges.
- **Token Transfers**: Validate recipient addresses to prevent accidental token loss.
- **Input Validation**: Check inputs thoroughly to prevent invalid operations and potential exploits.
- **Gas Limit**: Some functions may require a higher gas limit due to potential iterations or complex computations.

## License

This project is licensed under the MIT License. See the SPDX-License-Identifier tag in the contract file for more details.
