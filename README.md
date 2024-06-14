# Token Creation

This project program is all about Token Creation, as in the title says! 

## Description

Written in Solidity, a programming language used to create smart contracts on the Ethereum blockchain, this program is a straightforward contract. The code consists of 2 main sections: burning and minting tokens. This application can be used as a springboard for more complicated projects in the future and provides a clear and basic introduction to Solidity programming.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

```javascript
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
    string public tokenName = "KRILL";
    string public tokenAbbrv = "KRL";
    uint public totalSupply = 0;


    // mapping variable here
    mapping (address => uint) public balances;


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

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile <yourfilename>.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Then, click on the "Deploy" button.

Once the contract is deployed, you can interact with it by entering the amount you would want to mint/burn in the account. You make update the values by pressing the variable buttons.

## Authors

Jan Kristoffer L. Almniniana 
