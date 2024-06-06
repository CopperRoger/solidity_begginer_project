# My Token

This Solidity program is a simple program that demonstrates the basic functionality of the a token in blockchain.

## Description

This program is a simple contract MyToken is a simple token system built on the Ethereum blockchain. It includes basic functionalities to mint (create) and burn (destroy) tokens and tracks essential details such as the token's name ("Best Token"), abbreviation ("BT"), and total supply.
## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., MyToken.sol). Copy and paste the MyToken.sol into the file:

```javascript

// SPDX-License-Identifier: MIT
pragma solidity 0.8.25;

contract MyToken {

    // public variables here
    string public tokenName = "Best Token";
    string public tokenAbbrv= "BT";
    uint public totalSupply=0;

    // mapping variable here
    mapping(address=> uint) public balances;

    // mint function
    function mint(address _address, uint _value) public {
      totalSupply += _value;
      balances[_address] += _value;
    }

    // burn function
    function burn(address _address , uint _value) public{
      if(balances[_address] >= _value){
         totalSupply -= _value;
         balances[_address] -= _value;
      }
    }

}
```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.25" , and then click on the "Compile MyToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the checking values of public variables including totalSupply and balances associated with addresses.

You can mint any amount to different addresses with passing the address and number of tokens to the "mint" function.You can also use "burn" function to burn token from a given address given it has enough in balance.


## Authors

Akshit Sharma
