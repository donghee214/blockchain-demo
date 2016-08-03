```javascript

//header to add web3 API
if (typeof web3 !== 'undefined') {
  web3 = new Web3(web3.currentProvider);
} else {
  // set the provider you want from Web3.providers
  web3 = new Web3(new Web3.providers.HttpProvider("http://localhost:8545"));
}

//retreieve transaction details from an address 
function getTransaction(){
  //retreieve input of either the trasaction hash, or the specific transaction number in a specified block
	var transaction = web3.eth.getTransactionFromBlock($(".Number1").val(), ($(".TransactionNumber").val()));
	//start the string of text on a new line for new information
	var transaction2 = JSON.stringify(transaction).replace(/,/g ,"<br>")
	$(".info").html(transaction2);
}


```

```html
<div class="info">
  
</div>
```
