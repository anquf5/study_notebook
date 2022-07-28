# JS面试题

### null和undefined

* #### type区别：null - object, undefined - undefined
* #### **出现undefined的情况：**

1.  某个对象被声明但没赋值

    let o; console.log(o) //undefined
2.  对象上某一个属性不存在

    let obj = {} console.log(obj.a) //undefined
3.  函数调用时候少参数

    function fn(a, b){ console.log(a, b) } fn(4) //undefined
4.  常规函数的默认返回值（构造函数除外）

    function a(){ console.log("11") } console.log(a());

* **出现null的情况**

1. 手动释放内存 let obj = {} obj = null
2. 作为函数参数（此参数不是对象）
3. 原型链的顶端

### filter

```
let a = [1,2,3,14,15]
// 1. current 当前值，index 当前值下标，array 数组对象
let b =  a.filter((current, index, array) => {
	return current < 10
})
console.log(a)
console.log(b)
```

### forEach和map

{% hint style="info" %}
foreach&#x20;

1. 无返回值
2. 不能break打断&#x20;
3. 遍历的值是value
{% endhint %}

```
let arr = ['a', 'b', 'c']
let res = arr.forEach(element => {
	return element + '1' // undefined
})
```

{% hint style="info" %}
map&#x20;

1. 有返回值（数组），默认return undefined
2. 接收的参数是一个函数（key，value）
3. 不能用break打断
{% endhint %}

```
let arr = ['a', 'b', 'c']
let res = arr.map((value, key)=> {
	return value + '1' // 
})
console.log(res) // a1, b1, c1
```

### JS递归求和1-100

```
function add(num1, num2){
	let num = num1 + num2
	if(num2 + 1 > 100){
		return num
	}else{
		return add(num, num2 + 1)
	}
}
let sum = add(1,2)
console.log(sum)
```
