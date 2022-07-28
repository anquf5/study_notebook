# JS原型与原型链

原型 prototype 原型链 _proto_ \[\[prototype]]

**原型是函数特有，常规对象和数组不存在**

```
function fn(){
}
fn.prototype.name = "小明"
fn.prototype.fn2 = function(){ console.log ("111")}
```

**原型链是函数，对象，数组都有的**

```
function Person(){    	
}
Person.prototype.name = '小明'
Person.prototype.age = 18
Person.prototype.getAge = function(){
	console.log(this.age)
}
let person1 = new Person() //被构造的实例
person1.age = 28
console.log(person1.name) //28
person1.getAge()
console.log(person1.demo) //undefined
```

原型链查找规则：从当前实例属性查找，找到就返回，否则顺着原型链一层一层网上找，直到找到null为止，如果到null都没找到，则报错

找私有属性：

```
let item;
for(item in person1){
	if(person1.hasOwnProperty(item)){
		console.log(item)
	}
}
```

被构造的person1，\_proto\_是指向函数的prototype
