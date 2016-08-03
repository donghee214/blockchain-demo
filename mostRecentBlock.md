```javascript
//header to add web3 API
if (typeof web3 !== 'undefined') {
  web3 = new Web3(web3.currentProvider);
} else {
  // set the provider you want from Web3.providers
  web3 = new Web3(new Web3.providers.HttpProvider("http://localhost:8545"));
}

//retreieve the latest added block
function latestBlock(){	
    //store the integer in "number"
		var number = web3.eth.blockNumber;
		$(".Number").empty();
		//display "number" in empty div
		$(".Number").html(number);
}
		```
		
		```html
		<div class="Number">
		
		</div>
		```
