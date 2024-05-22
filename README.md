# PROJECT SOLIDITY
## OVERVIEW
This is a simple project for a token called "PHILIPPINE PESO" with the abbreviation of "PHP". The project defines several public variables to store the details about the token, including the token name, abbreviation, and total supply. The project also includes a mapping of addresses to balances, it also includes two functions: BURN and MINT. 
## CONTRACT DETAILS 
```solidity
contract MyToken {
    string public tokenName = "PHILIPPINE PESO";
    string public tokenAbbrv = "PHP";
    uint public totalSupply = 0;
}
```
Defines the name of the contract, which is "MyToken". It also includes the public variables that represent the details of the token, wherein <mark> tokenName <mark/> defines the name of the token and initializes it with the value "PHILIPPINE PESO", and _tokenAbbrv_ represents the abbreviation of the token and initializes it with the value "PHP". While the _totalSupply_ represents the token's total exists in circulation. 
## MAPPING ADDRESS
```solidity
   mapping(address => uint) public balances;
```
Defines a public mapping called  _balances_  that maps addresses to balances, which keeps track of the balance of each address that holds the token.

## MINT FUNCTION
```solidity
function mint(address _address, uint _amount) public  {
        totalSupply += _amount;
        balances[_address] += _amount;
    }
```
The _mint_ function increases the token's total supply and the address's balance. 

## BURN FUNCTION 
```solidity
 function burn(address _address, uint _amount) public {
        if (balances[_address] >= _amount) {
            totalSupply -= _amount;
            balances[_address] -= _amount;
        }
```
The _burn_ function decreases the token's total supply and the address's balance.
