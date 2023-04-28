# SolidityToken
# Create a Token in Solidity

This Solidity program is a simple program that tries to create a token with different functionalities such as minting and burning. The purpose of this program is to serve as a starting point for those who are new to Solidity and want to get a feel for how it works.

## Description

This program contains a simple contract written in Solidity; it contains variables that stores the details of a coin such as token name, token abbreviation and total supply. The contract can also map addresses to the contract and has a mint funtion that increases the total supply by a number and increases the balance of the address by that amount. The burn function in the contract can deduct the value from the total supply and from the balance of the address; it has conditionals to make sure the balance of account is greater than or equal to the amount that is supposed to be burned.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., MyToken.sol). Copy and paste the following code into the file:

```javascript
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
        string public tokenName="NEDER";
        string public tokenAbbr="NDR";
        uint public totalSupply=0;

    // mapping variable here
        mapping(address=> uint) public balances;
        
    // mint function
    function mint(address _address, uint _value) public{
        totalSupply += _value;
        balances[_address] +=_value;
    }

    // burn function
    function burn(address _address, uint _value) public{
        if (balances[_address]>=_value){
        totalSupply -= _value;
        balances[_address] -=_value;
        }
    }
}

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile myToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by experimenting around in the deploy and run transations tab. Under the deployed contracts, you can try to edit the address and value to understand how the functions work.
## Authors

Nathalie



