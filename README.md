# MyToken Contract

The MyToken contract is a Solidity smart contract that represents a basic token system. It allows for the minting and burning of tokens, as well as tracking the token balances of different addresses.

## Requirements

1. The contract stores public variables that hold the details of the coin, including the token name, token symbol, and total supply.
2. The contract includes a mapping that associates addresses with their token balances.
3. The contract provides a mint function that takes an address and a value as parameters. This function increases the total supply by the specified value and increases the balance of the sender's address by that amount.
4. The contract includes a burn function that works in the opposite way of the mint function. It takes an address and a value as parameters, deducting the specified value from the total supply and the balance of the sender's address.
5. The burn function includes conditionals to ensure that the sender's balance is greater than or equal to the amount that is supposed to be burned.

## Usage

### Public Variables

- `coinName`: A string variable representing the name of the token.
- `coinSymbol`: A string variable representing the symbol or abbreviation of the token.
- `totalCoinSupply`: An unsigned integer variable representing the total supply of the token.

### Functions

- `mint(address newAddress, uint newValue)`: Mints new tokens and assigns them to the specified address. Increases the total supply by the specified value and updates the balance of the new address.
- `burn(address targetAddress, uint burnValue)`: Burns tokens from the specified address. Deducts the specified value from the total supply and updates the balance of the target address. The burn is only allowed if the target address has a sufficient balance.

## License

This contract is released under the MIT License.
