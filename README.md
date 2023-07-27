Tokens 

Artificial Token. It's a simple program that stores the input and shows the output of the user. 

Description

It's a program that stores a value and burns a value of a token. It's a simple program that stores and output all the stored data. 
This program serves as a simple and straightforward introduction to Solidity programming, and can be used as a stepping stone for more complex projects in the future.
            

Getting Started

Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. 
Save the file with a .sol extension (e.g., Token.sol). Copy and paste the following code into the file:

    // SPDX-License-Identifier: MIT
    pragma solidity 0.8.18;

    contract MyToken {

        // public variables here
        string public tokenName = "SOLID"; 
        string public tokenAbbrv = "SLD"; 
        uint public totalSupply = 0; 
    
        // mapping variable here
        mapping(address => uint) public balance;  
    
        // mint function
        function mint(address _address, uint _value) external {
            balance[_address] += _value;
            totalSupply += _value; 
    
        }
    
        // burn function
        function burn(address _address, uint _value) external {
            if (balance[_address] >= _value) {
                balance[_address] -= _value;
                totalSupply -= _value; 
            }
        }
    }

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. 
Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile Tokens.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. 
Select the "MyTokens" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with the following functions by calling it. 
Click on the "MyToken" contract in the left-hand sidebar, and then click on the "Mint" function. Mint function stores users address and input value. 
Once the user mintted. Call the the balanace by inputting the address that is inputted once in the mint function to show the balanace value. 
"Burn" function is another function to be used if the user wants to burn a value of its token. Simply by inputting the same address and the value its want.
Once called it will subtract the current value from the inputted value. 
Finally, call the "tokenName", "tokenAbrv", and "totalSupply" to see the value of the token.

Authors

Renan Ashley Alcantara

@metacraftersio

License

This project is licensed under the MIT License - see the LICENSE.md file for details
