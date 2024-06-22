MY TOKEN
This Solidity program is a simple program writtened to create token in blockchain using solidity and mint and burn the the total supply of tokens and learn more about the tokens.

Description
This program is a simple contract written in Solidity, a programming language used for developing smart contracts similarly in this program we created smart contract named my token and wrote some variables inside it and then created functions to mint and burn total supply ok tokens.
Getting Started
Executing program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/. 

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;
contract MyToken {
    // public variables here
      string public token_name = "Ether";
  string public token_abbrv = "Ethereum";
  uint public total_supply = 1;

    // mapping variable here
mapping(address=> uint) public balances;
    // mint function
    function mint(address addresss, uint value) public  {
      total_supply += value;
      balances[addresss] += value;
    } 
      // burn function
      function burn(address addresss, uint value) public  {
        if(balances[addresss]>=value){
          total_supply -= value;
      balances[addresss] -= value;

        }
      
    } 

}
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile HelloWorld.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "my token" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the burn and mint function. 
Authors

License
This project is licensed under the MIT License - see the LICENSE.md file for details
