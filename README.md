# MyToken

This Solidity program demonstrates a basic implementation of a token system, showcasing the minting and burning functionalities of tokens. The purpose of this program is to serve as a starting point for those who are new to Solidity and want to understand how to create and manage tokens on the Ethereum blockchain.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has functions to mint new tokens, burn existing tokens, and keep track of token balances. This program serves as a straightforward introduction to Solidity programming, and can be used as a stepping stone for more complex projects in the future.

## Getting Started

### Executing Program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at [Remix Ethereum](https://remix.ethereum.org/).

1. Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a `.sol` extension (e.g., `MyToken.sol`). Copy and paste the following code into the file:

    ```solidity
    // SPDX-License-Identifier: MIT
    pragma solidity ^0.8.18;

    contract MyToken {
        // public variables here
        string public tokenName = "META";
        string public tokenAbbrv = "MTA";
        uint public totalSupply = 0;

        // mapping variable here
        mapping(address => uint) public balances;

        // mint function
        function mint(address _address, uint _value) public {
            totalSupply += _value;
            balances[_address] += _value;
        }

        // burn function
        function burn(address _address, uint _value) public {
            if (balances[_address] >= _value) {
                totalSupply -= _value;
                balances[_address] -= _value;
            }
        }
    }
    ```

2. To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile MyToken.sol" button.

3. Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

4. Once the contract is deployed, you can interact with it by calling the `mint` and `burn` functions. Click on the "MyToken" contract in the left-hand sidebar, and then click on the desired function. Enter the necessary parameters and click on the "transact" button to execute the function.

## Authors
Adrian Oraya

## License

This project is licensed under the MIT License - see the LICENSE.md file for details.
