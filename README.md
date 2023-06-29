# MyToken

MyToken is a Solidity contract that represents a basic token with the ability to mint (create) and burn (destroy) tokens. It allows users to keep track of balances and manage the total supply of tokens.

## Requirements

1. The contract has public variables that store the details about the coin, including the token name, token abbreviation, and total supply.
2. The contract includes a mapping of addresses to balances, which allows tracking the token balance for each address.
3. The contract provides a `mint` function that increases the total supply by a specified value and increases the balance of the specified address by the same amount.
4. The contract includes a `burn` function that decreases the total supply and the balance of the specified address by a given value.
5. The `burn` function includes conditionals to ensure that the balance of the address is greater than or equal to the amount to be burned.

## Usage

1. Deploy the `MyToken` contract to a Solidity-compatible blockchain network.
2. Interact with the contract using a compatible wallet or smart contract interaction tool.

### Public Variables

- `tokenName`: A string variable representing the name of the token.
- `tokenAbbrv`: A string variable representing the abbreviation of the token.
- `totalSupply`: An unsigned integer variable representing the total supply of tokens.

### Functions

- `mint(address _address, uint _value)`: A function that mints new tokens and increases the total supply and balance of the specified address.
  - `_address`: The address to which the tokens will be minted.
  - `_value`: The amount of tokens to be minted.
- `burn(address _address, uint _value)`: A function that burns (destroys) tokens by reducing the total supply and the balance of the specified address.
  - `_address`: The address from which the tokens will be burned.
  - `_value`: The amount of tokens to be burned.

### Example Usage

```solidity
// Deploy the MyToken contract

// Mint 100 tokens for address 0x123abc
mint(0x123abc, 100);

// Burn 50 tokens from address 0x123abc
burn(0x123abc, 50);
```
