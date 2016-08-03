```javascript
///Retreieve accounts stored on local computer

if (typeof web3 !== 'undefined') {
  web3 = new Web3(web3.currentProvider);
} else {
  // set the provider you want from Web3.providers
  web3 = new Web3(new Web3.providers.HttpProvider("http://localhost:8545"));
}

function getAccounts(){
	//uses web3.js API to store the account address in "accounts"
	var accounts = web3.eth.accounts;
	console.log(accounts);
	var tempStr = "";
	//sorts through hex characters and puts a line inbetween the seperate account addresses
	for (var i = 0; i < accounts.length; i++) {
		tempStr += accounts[i] + ",\n"
	}
		$(".AccountsOnNode").html(tempStr.substring(0, tempStr.length - 2));
	
}
```
