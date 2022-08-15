# Sample Hardhat Project

This project demonstrates a basic Hardhat use case. It comes with a sample contract, a test for that contract, and a script that deploys that contract.

Try running some of the following tasks:

```shell
npx hardhat help
npx hardhat test

```

```.delegatecall()``` is heavily used within proxy (upgradeable) contracts. Since smart contracts are not upgradeable by default. But, since it modifies the storage of the contract calling the function, there are some nasty attacks that can be designed if it is not properly implemented. We will now simulate an attack

If your tests are passing the owner address of good contract was indeed changed, since we equate the value of the ```owner``` variable in ```Good``` to the address of the ```Attack``` contract at the end of the test.

# How we can prevent this

Use stateless library contracts which means that the contracts to which you delegate the call should only be used for execution of logic and should not maintain state. This way, it is not possible for functions in the library to modify the state of the calling contract.
