# JS防抖与节流

### 防抖

{% hint style="info" %}
将多次操作变成一次，只允许一个操作存在， 固定时间内事件只允许发生一次
{% endhint %}

```
 <input placeholder="请输入电话">
 <script>
	 let telInput = document.querySelector('input')
	 telInput.addEventListener('input', (e) => {
		 console.log('发起请求')
	 })
 </script> //如果速度过快会发生抖动

解决：
let telInput = document.querySelector('input')
telInput.addEventListener('input', antiShake(demo, 2000))
//防抖封装
function antiShake(fn, wait){
	let timeOut = null;
	return args => {
		if(timeOut) clearTimeout(timeOut)
		timeOut = setTimeout(fn, wait);
	}
}
function demo(){
	console.log('发起请求')
}
```

### 节流&#x20;

{% hint style="info" %}
保证一定时间内的只调用一次处理函数， 把多个事件合为一个 应用场景： 1. 提交表单，2. 高频监听事件
{% endhint %}

```
let box = document.querySelector(".box")
box.addEventListener("touchmove",(e) => {
	console.log("发起请求")
})

function throttle(event, time) {
	let timer = null
	return function(){
		if(!timer){
			timer = setTimeout(() => {
				event();
				timer = null;	
			}, time);
		}
	}
```

### 通过时间戳
