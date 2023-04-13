# MyToken

This is a simple Solidity program that demonstrates the basic syntax and function working of the Solidity programming language. The purpose of this program is to serve as a starting point for those who are new to Solidity and want to understand about token minting and get a feel for how it works.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has two functions - mint() and burn(). mint() demonstrates how tokens are created and burn() demonstrates how tokes can be destroyed. The contract returns the public variables as functions that returns the value stored in them, like name,symbol and totalSupply,this is an advantage of having public variables in solidity that they will be treated as functions returning the value stored in them. This program serves as a simple and straightforward introduction to tokens, and can be used as a stepping stone for more complex projects in the future.

## Getting Started

### Installing

* To download the program you can fork the project or directly go to the file : https://github.com/chaiSEth/metacraftersAssignment/blob/main/MyToken.sol and copy the code. You can use Remix IDE to execute it. Steps for execution is below.

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., MyToken.sol). Copy and paste the following code into the file:


    // SPDX-License-Identifier: MIT
    pragma solidity 0.8.18;

    contract MyToken {
        // public variables here
        string public name = "myERC";
        string public symbol = "CSN";
        uint256 public totalSupply;
        // mapping variable here
        mapping(address => uint256) public balanceOf;

        function mint(address sender, uint256 amount) external {
            balanceOf[sender] += amount;
            totalSupply += amount;
        }
        // burn function
        function burn(address sender, uint amount) external{
            require(balanceOf[sender] >= amount,"Insufficient tokens to burn");
            balanceOf[sender] -= amount;
            totalSupply -= amount;
        }
     }

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile MyToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the name and symbol function. Click on the "MyToken" contract in the left-hand sidebar, and then click on the "mint" function by providing any valid address and the number tokens you want to mint. Once minting is successfully you can check by providing the same address to "balanceOf", this shows the number of tokens minted. Finally, click on the "burn" button to execute the function and destroy the tokens, parameters are the address for which the tokens needs to be burnt and the number of tokens to burn. The updated balance of the address can be checked in "balanceOf".

## Help

Contact the author

## Authors

Contributors names and contact info

Chaitra Shringa  
https://twitter.com/ChaitraShringa?t=AOlhlJ2OWd3FI9uGiyfv-A&s=09


## License

This project is licensed under the MIT License.
