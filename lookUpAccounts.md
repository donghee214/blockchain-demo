```javascript

//header to add web3 API
if (typeof web3 !== 'undefined') {
  web3 = new Web3(web3.currentProvider);
} else {
  // set the provider you want from Web3.providers
  web3 = new Web3(new Web3.providers.HttpProvider("http://localhost:8545"));
}


//get balance of accounts
function getBalanceOfAcc(){
	//stores the amount of gas for respective account in "balance"
	var balance = web3.eth.getBalance($(".myInput").val());
	//converts the denomination of gas into ether
	var balance = balance/1000000000000000000;
	$(".balance").html("ether: " + balance);
	console.log(balance); 
	console.log(balance.toString(10));

}
```
```html
//input field for address of the account 
<input type="text" class="myInput" placeholder="address"> 
```
