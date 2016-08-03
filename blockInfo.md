
```javascript

//header to add web3 API
if (typeof web3 !== 'undefined') {
  web3 = new Web3(web3.currentProvider);
} else {
  // set the provider you want from Web3.providers
  web3 = new Web3(new Web3.providers.HttpProvider("http://localhost:8545"));
}


var info = web3.eth.getBlock(3150);
console.log(info);
var info = JSON.stringify(transaction).replace(/,/g ,"<br>");
$(".blockInfo").html($(".info"));


```


```html
<div class="blockInfo">

</div>
```
