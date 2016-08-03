```javascript
function getAccounts(){
	var accounts = web3.eth.accounts;
	console.log(accounts);
	//$(".AccountsOnNode").html(accounts);
	var tempStr = "";
	for (var i = 0; i < accounts.length; i++) {
		tempStr += accounts[i] + ",\n"
	}
		$(".AccountsOnNode").html(tempStr.substring(0, tempStr.length - 2));
	
}
```
