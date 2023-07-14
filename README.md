# -MyToken---ERC20-Token-Contract-with-Mint-and-Burn-Functions-
This repository contains a Solidity smart contract for the "MyToken" ERC20 token. It includes functionalities to mint and burn tokens, keeping track of the total supply and individual balances. This contract serves as a foundation for managing tokens on the Ethereum blockchain.
This project is a Solidity smart contract for the "MyToken" ERC20 token. It enables token minting and burning operations, while tracking the total token supply and individual balances. The contract serves as a fundamental building block for managing tokens on the Ethereum blockchain.

Process and Steps:

Contract Initialization:

The contract is initialized with the name "MyToken" and deploys an ERC20 token on the Ethereum blockchain.
It sets the initial values for public variables, such as tokenName, tokenAbbrv, and totalSupply.
Additionally, a mapping named balances is created to associate addresses with their token balances.
Minting Tokens:

The mint function is provided to create new tokens and distribute them to a specified address.
When called, the function takes two parameters: _address (the recipient address) and _value (the number of tokens to be minted).
Within the function, the total supply is increased by _value, and the _value is added to the balance of _address in the balances mapping.
Burning Tokens:

The burn function is implemented to remove tokens from circulation and decrease an address's balance.
The function requires two parameters: _address (the owner of the tokens) and _value (the number of tokens to be burned).
It first checks if the balance of _address is greater than or equal to _value.
If the condition is met, the total supply is decreased by _value, and the _value is subtracted from the _address balance in the balances mapping.
The contract has state variables to keep track of the token information such as token Name, token abbreviation, total supply of tokens in the network and balances mapping that maps an address to the amount of tokens that address holds. This contract also has functions like mint and burn to modify the amount of tokens in the network.

function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] +=_value;
}
function burn(address _address, uint _value) public {
    if (balances[_address] >= _value) {
        totalSupply -= _value;
        balances[_address] -=_value;
    }   
}
This program serves as a simple and straightforward introduction to how tokens work

Getting Started
Executing program
STEP 1
You can use Remix, an online Solidity IDE to run this program. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., MyToken.sol). Copy and paste the code present in Token.sol

STEP 2
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar and then click on the "Compile myToken.sol" button.

STEP 3
Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, then click the "Deploy" button.

STEP 4
Once the contract is deployed, you can interact with it by calling the various functions. For starters click on the "MyToken" contract in the left-hand sidebar, and then click on the "mint" function to add tokens to an address.
Authors
Metacrafter Student
Aditya Kumar
