在js的世界中，一切都是对象，但还有些对象与其他对象不一样，例如number,string,null,undefine，function,boolean等。因此有必要把他们区分一下。

Data()
时间戳：是一个自增的整数，表示从1970年开始到现在的毫秒数，假设浏览器所在电脑的时间是准确的，那么世界上无论哪个时区的电脑，它们此刻产生的时间戳数字都是一样的，所以，时间戳可以精确地表示一个时刻，并且与时区无关。

正则表达式
先不慌学这个

JSON
可以将一个对象写成json,例如
var xiaoming={
	name:"mingge",
	age:18,
	gender:true,
	skills:['java','javascript','php']
}
使用方法JSON.stringify(xiaoming);
也可以添加参数JSON.stringify(xiaoming,null,'');第二个参数可以使一个方法，用来处理每个键值对。也可以使用一个数组，用来获取想要的键值对。
拿到一个JSON格式的字符串，我们直接用JSON.parse()把它变成一个JavaScript对象：
JSON.parse('{"name":"小明","age":14}');