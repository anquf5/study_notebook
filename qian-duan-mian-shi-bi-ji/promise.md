# Promise

```
// 同步执行
const promise = new Promise((resolve, reject) => {
	console.log(1)
	resolve();
	console.log(2);
})
// then（） 异步执行
promise.then(() => {
	console.log(3)
})    
console.log(4) //1243
```
