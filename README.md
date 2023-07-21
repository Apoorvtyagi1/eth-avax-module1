# eth-avax-module1
# Functions and Errors - ETH + AVAX
This is a solidity program which contains a smart contract diplaying the basic functions of the require(), revert(), and assert functions.

## Description
This contract on solidity shows an ecample of the three major error handling functions in solidity that are require(), revert(), and assert functions. 
The program is based in a situation where we have to check the age of the user. 
If the age of the user i above 18, then the requested transaction of be done to their account, if not then the error will be handled using the functions.
And it will handle divide by zero error.

## Getting Started

### Executing the program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar.
Save the file with a .sol extension (e.g., contract.sol). Copy and paste the following code into the file:

```
// pragma solidity ^0.8.0;

contract salary {

    uint public totalsalaryrecived;
    mapping(address => bool) public hassalarygiven;

    function salarygiven() public {
        require(!hassalarygiven[msg.sender], "Already Given"); 

        totalsalaryrecived++;
        hassalarygiven[msg.sender] = true;

        if (totalsalaryrecived > 50) {
            revert("employee limit exceeded"); 
        }

        assert(totalsalaryrecived <= 50); 
    }
}
```
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar.

Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile contract.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the contract from the dropdown menu, and then click on the "Deploy" button.

After that you can put your credentials that will be your age, amount of tokens you want, and 2 integers to perform division.

After that go onto each fucntions RequireCheck(), RevertCheck() and AssertCheck() put the required inputs and press transact.

## Authors 
Apoorv Tygai


tyagiapoorv4@gmail.com 
## Lisence
This project is licensed under the MIT License - see the LICENSE.md file for details
