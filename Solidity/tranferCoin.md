

```javascript

contract MyToken is owned{
	//initialize variables
	string public standard = 'Token 0.1'; 
	string public name;
	string public symbol;
	uint8 public decimals;
	uint public totalSupply;
	
	//create an array of balances
	mapping (address => uint256) public balanceOf;
	mapping (address => mapping (address => uint256)) public allowance;
	
	
	//create coin
	function Mytoken(
		uint256 initialSupply, 
		string tokenName, 
		uint8 decimalUnits,
		string tokenSymbol,
		address centralMinter
	)
	
	//transfer asset to given address and value
	function transfer (address _to, uint256 _value){
		//if senders balance is less than transfer value, throw
		if (balanceOf[msg.sender] < _value) throw;
		if (balanceOf[_to] + _value < balanceOf[_to]) throw;
		//subtract the amount of sender
		//add the amount to the receiver
		balanceOf[msg.sender] -= _value;
		balanceOf[_to] += _value;
		Transfer(msg.sender, _to, _value);
	}
}

```
