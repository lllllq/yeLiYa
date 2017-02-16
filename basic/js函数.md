在js中，函数也是一个对象。

1 arguments只能在函数内部使用，它指向传入这个函数的参数。类似于Array，但并不是Array.最主要的用途是用来写可选参数的函数。例：
function abs(a,b,c){
	if(arguments.length==2){
		c=b;
		b=null;
	}
}
通过此方法可将中间的参数b给忽略掉。

2 rest参数
是在ES6新增的标准，一个数组，可以获取多余的参数
function abs(a,b,...rest){
	console.info(rest);
}

3 let块级作用域， const 用来定义常量，都是在ES6中新增的标准

4 方法：在一个对象中绑定函数，就叫做方法，绑定到对象上的方法和普通的函数没有什么区别，但是它在内部使用了一个this关键字。如果在函数内部使用this关键字，它会指向哪里呢？答案是视情况而定。
var xiaoming={
	name:"xiaoming",
	birthdy:1995,
	age=function(){
		var y=new Data().getFullYear();
		return y-this.birthdy;
	}
}
xiaoming.age; //function xiaoming.age()
xiaoming.age(); //得到实际的年龄
在上面的例子中，this指向了xiaoming这个对象，这是我们所期待的情况。
var getAge=function(){
	var y=new Data().getFullYear();
	return y-this.birthdy;
}

var xiaoming = {
    name: '小明',
    birth: 1990,
    age: getAge
};

xiaoming.age(); //实际年龄
xiaoming.age;  //[function:getAge]
getAge();  //error
在这个例子中，在单独调用getAge()时，this指向了全局变量,即window.
总结：如果以对象的形式调用this,会指向当前调用它的对象，单独调用时则会指向全局对象。在严格模式下，this有时也会指向undefine.
程序员可以自己控制this的指向，方法就是使用函数自带的apply或者call方法。例如
getAge.apply(xiaoming,[]);  //apply有两个参数，第一个是this需要让this指向的对象，第二个是函数自己的参数，用数组包起来。
call方法和apply基本相似，唯一区别是apply把参数打包成Array传入，call按顺序传入。

5 闭包
简单来说就是函数的返回结果还是一个函数，闭包有个很强大的功能，在别的语言中，可以使用private来修饰一个内部变量。但js中没有class机制，只有函数，因此无法使用private,但我们可以使用闭包实现此功能。另外还可以把多个参数的函数变为一个参数。

箭头函数

generator(生成器) 简单来将就是一个可以返回多次的函数
function* foo(x){
	yield x+1;
	yield x+2;
	return x+3;
}