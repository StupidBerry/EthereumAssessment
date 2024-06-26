# MyToken

This Solidity program is a simple ehtereum contract program that demonstrates the basic syntax and functionality of the Solidity programming language. The purpose of this program is to serve as a starting point for those who are new to Solidity and want to get a feel for how it works.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. .This program has two functions , i.e, mint and burn function that are used to add and substract from totalsupply. This program serves as a simple and straightforward introduction to Solidity programming, and can be used as a stepping stone for more complex projects in the future.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

```javascript
contract MyToken {

    // public variables here
    string public tname = "ARYAN";
    string public tabbrv = "ARY";
    uint public totalsup = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint(address addr , uint val) public {
      totalsup += val;
      balances[addr] += val;
    }

    // burn function
      function burn(address addr , uint val) public {
       if(balances[addr]>=val) {

       totalsup -= val;
       balances[addr] -= val;
       }
    }


}

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile HelloWorld.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "HelloWorld" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the sayHello function. Click on the "HelloWorld" contract in the left-hand sidebar, and then click on the "sayHello" function. Finally, click on the "transact" button to execute the function and retrieve the "Hello World!" message.

## Authors

Aryan Khanduri
(https://www.instagram.com/aryankindastoopid/)


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
