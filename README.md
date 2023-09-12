# SolidityProject
This Solidity program is likely a project "SolidityProject" that involves writing and deploying smart contracts on the Ethereum blockchain using the Solidity programming language.

# Description
The provided code is a Solidity contract for a basic token on the Ethereum blockchain. It includes details about the token, maintains a balance of tokens for each address, and has functions to mint (create) and burn (destroy) tokens. The mint function increases the total supply and the balance of a specified address, while the burn function decreases them, provided the balance is sufficient. This contract can be used in projects requiring a custom token with minting and burning capabilities.

# Getting Started
### Executing program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., MyToken.sol). Copy and paste the following code into the file:
```javascript
pragma solidity 0.8.18;

contract MyToken {
    // public variables here
    string public tokenName = "CRAFTER";
    string public tokenAbbrv ="CRFTR";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint (address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }
    
    // burn function
    function burn (address _address, uint _value) public {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
             balances[_address] -= _value;
        }
    }
}
```
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18", and then click on the "Compile MyToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the MyToken function. 

# Authors
Marl Shane G. Esteron

# License
This project is licensed under the Marl Shane Esteron License 
