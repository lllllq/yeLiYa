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

