
```javascript

//contract parameters
contract MyToken is owned{
	//initialize variables
	string public standard = 'Token 0.1'; 
	string public name;
	string public symbol;
	uint8 public decimals;
	uint public totalSupply;
	
	//creates an array with all the balances
	mapping (address => uint256) public balanceOf;
	mapping (address => mapping (address => uint256)) public allowance;
	
	//create token
	function Mytoken(
		uint256 initialSupply, 
		string tokenName, 
		uint8 decimalUnits,
		string tokenSymbol,
		address centralMinter
	)
		//sets target of the minted token to self
		//specifies amount
		function mintToken(address target, uint256 mintedAmount) onlyOwner{
		balanceOf[target] += mintedAmount;
		totalSupply += mintedAmount;
		Transfer(0, owner, mintedAmount);
		Transfer(owner, target, mintedAmount);
	}
	
	
	
	```
