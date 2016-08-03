

```javascript

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
	
	function Mytoken(
		uint256 initialSupply, 
		string tokenName, 
		uint8 decimalUnits,
		string tokenSymbol,
		address centralMinter
	)
	
	function transfer (address _to, uint256 _value){
		if (balanceOf[msg.sender] < _value) throw;
		if (balanceOf[_to] + _value < balanceOf[_to]) throw;
		balanceOf[msg.sender] -= _value;
		balanceOf[_to] += _value;
		Transfer(msg.sender, _to, _value);
	}
}

```
