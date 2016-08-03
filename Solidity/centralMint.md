
```javascript

//initializes the coin
contract MyToken is owned{
	/*variable of the token*/
	string public standard = 'Token 0.1'; 
	string public name;
	string public symbol;
	uint8 public decimals;
	uint public totalSupply;
	
	/* Creates an array with all balances*/
	mapping (address => uint256) public balanceOf;
	mapping (address => mapping (address => uint256)) public allowance;
	
	/*This generates a public event on the blockchain that will notify client*/
	event Transfer(address indexed from, address indexed to, uint256 value);
	
	
	//create token function
	function Mytoken(
		//token parameters
		uint256 initialSupply, 
		string tokenName, 
		uint8 decimalUnits,
		string tokenSymbol,
		address centralMinter
	){	
		//if there is no central minter allocate to self
		if(centralMinter!=0) owner = centralMinter;
		//copy the details about the coin
		balanceOf[msg.sender] = initialSupply;
		totalSupply = initialSupply;
		name = tokenName;
		symbol = tokenSymbol;
		decimals = decimalUnits;
	}
	
	//if the sender of the contract is the owner create tokens
	function mintToken(address target, uint256 mintedAmount) onlyOwner{
		balanceOf[target] += mintedAmount;
		totalSupply += mintedAmount;
		Transfer(0, owner, mintedAmount);
		Transfer(owner, target, mintedAmount);
	}
}
```
