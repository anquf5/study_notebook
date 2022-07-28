# ES6相关面试题

### var、let、const

ES6不再推荐使用var

**1. var -- 声明提升**

```
console.log(num);
let num = 123; // 报错

console.log(num);
var num = 123; //undefined
```

**2. var -- 变量覆盖**

```
let num1 = 12
let num2 = 34
console.log(num1) //报错

var num1 = 12
var num1. = 34
consonle.log(num1) //34
```

**3. var -- 没有块级作用域**

```
function fn（）{
	for(var i = 0; i < 3; i++){
		console.log(i)
	}
	console.log(i) // 换成let会报错
}
```

### const

1. 声明后必须赋值， 否则报错（let，var可以）
2. 定义的值不能修改
3. 支持let的其他属性
4. 常量一般大写，用于全局

### 例题：

```
let a = 1; let b = 2;
```

**1. 如何用ES6调换两个值并不用第三方变量：**

```
[a, b] = [b, a] // 解构
```

**2. 如何使用ES6快速去重**

```
let arr = [12,23,34,12]
let item = [...new Set(arr)]
```
