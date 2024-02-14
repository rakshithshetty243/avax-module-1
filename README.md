# Solidity Contracts 

This repository contains two Solidity smart contracts:

1. **Vault**
2. **ERC20**

## 1. Vault

### Description
The `Vault` contract is designed to manage deposits and withdrawals of ERC20 tokens. It acts as a custodian where users can deposit their ERC20 tokens and receive shares in return. These shares can later be redeemed for the deposited tokens. 

### Functions
- `deposit(uint _amount)`: Allows users to deposit ERC20 tokens into the vault and receive shares in return.
- `withdraw(uint _shares)`: Allows users to withdraw ERC20 tokens by redeeming the shares they hold in the vault.

### Implementation Details
- The contract uses the `IERC20` interface to interact with ERC20 tokens.
- Upon deposit, shares are minted to the depositor based on their proportion of the total supply.
- Upon withdrawal, shares are burned and corresponding tokens are transferred back to the user.

## 2. ERC20

### Description
The `ERC20` contract is a basic implementation of the ERC20 token standard. It represents a fungible token with functionalities for transfer, approval, allowance management, minting, and burning.

### Functions
- `transfer(address recipient, uint amount)`: Allows token holders to transfer tokens to another address.
- `approve(address spender, uint amount)`: Allows token holders to approve another address to spend tokens on their behalf.
- `transferFrom(address sender, address recipient, uint amount)`: Allows approved addresses to transfer tokens from the sender's account to the recipient's account.
- `mint(uint amount)`: Allows the contract owner to mint new tokens.
- `burn(uint amount)`: Allows token holders to burn their own tokens.

### Implementation Details
- The contract maintains balances of token holders and allowances for spending.
- It emits events for transfers and approvals to allow external systems to track token movements.
- The token has a name (`Solidity`), symbol (`SOLBYEX`), and 18 decimal places precision.

## License
Both contracts are released under the MIT License.

