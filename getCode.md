```javascript

//header to add web3 API
if (typeof web3 !== 'undefined') {
  web3 = new Web3(web3.currentProvider);
} else {
  // set the provider you want from Web3.providers
  web3 = new Web3(new Web3.providers.HttpProvider("http://localhost:8545"));
}

function getCode(){
	var code = web3.eth.getCode("0x78dfc5983baecf65f73e3de3a96cee24e6b7981e");
	console.log(code);	
	var transaction2 = JSON.stringify(transaction).replace(/,/g ,"<br>")
	$(".Code).html(code);
}

```

```html
<div class="Code">

</div>
```
