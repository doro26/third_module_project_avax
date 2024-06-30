# third_module_project_avax

# myMintToken - ERC20 Token Contract

## Project Title
myMintToken

## Overview
myMintToken is an ERC20-compliant token built on the Ethereum blockchain. It allows an administrator to mint tokens, and any user to burn and transfer tokens. This contract is designed for simplicity and ease of integration into projects requiring basic token functionality.

## Description
The `myMintToken` contract provides a straightforward implementation of an ERC20 token, using OpenZeppelin's ERC20 standard. It includes essential features like minting, burning, and transferring tokens, making it suitable for various applications, such as creating custom tokens for decentralized applications, ICOs, or personal token experiments.

### Features:
- **Minting**: Only the contract's admin (deployer) can mint new tokens to any address.
- **Burning**: Any token holder can burn their own tokens to decrease their balance.
- **Transfer**: Users can transfer tokens between addresses.
- **Balance Inquiry**: Anyone can query the token balance of any address.

## Getting Started
### Using Remix IDE
1. **Compile the Contract**:
   - Open Remix IDE and navigate to the "Solidity Compiler" tab.
   - Compile `myMintToken.sol`.

2. **Deploy the Contract**:
   - Switch to the "Deploy & Run Transactions" tab.
   - Choose your preferred environment (e.g., JavaScript VM, Injected Web3).
   - Deploy the contract.

3. **Interact with the Contract**:
   - Use Remix's interface to call functions like `mint`, `burn`, `transferTokens`, and `balanceOfAddress`.



2. **Interact with the Contract**:
   - Use JavaScript and Ethers.js to interact with the deployed contract:
     
     const token = await MyMintToken.attach("deployed_contract_address");

     // Mint tokens (admin only)
     await token.mint("0xRecipientAddress", ethers.utils.parseUnits("100", 18));

     // Burn tokens
     await token.burn(ethers.utils.parseUnits("50", 18));

     // Transfer tokens
     await token.transferTokens("0xRecipientAddress", ethers.utils.parseUnits("10", 18));

     // Check balance
     const balance = await token.balanceOfAddress("0xAddress");
     console.log("Balance:", ethers.utils.formatUnits(balance, 18));
     


## License
This project is licensed under the MIT License. 


