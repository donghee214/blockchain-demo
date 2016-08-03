```javascript

//header to add web3 API
if (typeof web3 !== 'undefined') {
  web3 = new Web3(web3.currentProvider);
} else {
  // set the provider you want from Web3.providers
  web3 = new Web3(new Web3.providers.HttpProvider("http://localhost:8545"));
}


function getCode(){
	//get the address of the code from input
	var code = web3.eth.getCode("$(".myInput"));
	console.log(code);	
	//format the code by spacing out the string
	var code2 = JSON.stringify(code).replace(/,/g ,"<br>")
	$(".Code).html(code);
}

```

```html

<input class="myInput" />
<div class="Code">

</div>
```
