
```javascript

//header to add web3 API
if (typeof web3 !== 'undefined') {
  web3 = new Web3(web3.currentProvider);
} else {
  // set the provider you want from Web3.providers
  web3 = new Web3(new Web3.providers.HttpProvider("http://localhost:8545"));
}

//get blocknumber and use web3 API to store the string type in "info"
var info = web3.eth.getBlock($(".myInput"));
console.log(info);
//format the information to have spaces between different types of information
var info1 = JSON.stringify(info).replace(/,/g ,"<br>");
$(".blockInfo").html($(".info1"));

```


```html
<input class="myInput" />


<div class="blockInfo">

</div>
```
