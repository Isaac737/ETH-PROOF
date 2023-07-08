# MyToken

This contract implements a simple token with the ability to mint (create) and burn (destroy) tokens. The contract keeps track of the token name, abbreviation, total supply, and balances of token holders.


# Requirements
1. The contract has public variables for storing the token's name, abbreviation, and total supply.
2. An address to balance mapping is kept in the contract.
3. The mint function raises the balance of the sender's address and the total supply by the amount given.
4. The burn function subtracts a defined amount from both the overall supply and the balance of the sender's address.
5. Conditionals are built into the burn function to guarantee that the sender's balance is greater than or equal to the amount being burned.

# Usage
The contract provides the following functions:

mint(address _address, uint _value)
This function mints new tokens and assigns them to the specified address. It takes two parameters:

_address: The address to which the tokens will be minted.
_value: The number of tokens to mint.
The function increases the total supply by _value and updates the balance of _address accordingly.

burn(address _address, uint _value)
This function burns (destroys) existing tokens. It takes two parameters:

_address: The address from which the tokens will be burned.
_value: The number of tokens to burn.

Before burning the tokens, the function checks if the balance of _address is greater than or equal to _value. If the condition is satisfied, the function deducts _value from the total supply and updates the balance of _address accordingly. If the condition is not met, an error message is returned.

# Public Variables

The contract's public variables include the following:

tokenName
a string containing the token's name.

tokenAbbrv
a string that represents the token's shorthand.

totalSupply
The entire supply of tokens is represented by an unsigned integer.

# Mapping
The balances of token holders are stored in the contract via a mapping. Addresses are mapped to their corresponding token balances by the mapping 


# License
This contract is licensed under the MIT License. For more information, see the LICENSE file.
