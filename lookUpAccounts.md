```javascript

//header to add web3 API
if (typeof web3 !== 'undefined') {
  web3 = new Web3(web3.currentProvider);
} else {
  // set the provider you want from Web3.providers
  web3 = new Web3(new Web3.providers.HttpProvider("http://localhost:8545"));
}

function getBalanceOfAcc(){
	var balance = web3.eth.getBalance($(".myInput").val());
	var balance = balance/1000000000000000000;
	$(".balance").html("ether: " + balance);
	console.log(balance); 
	console.log(balance.toString(10));

}
```
```html
<input type="text" class="myInput" placeholder="address"> 
```
