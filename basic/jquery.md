使用jquery可以做到的事情
1 消除浏览器的差异，不需要写很多代码来适应不同的浏览器，如ajax中的XMLHttprequest
2 可以很方便的操作dom元素
3 轻松实现动画，修改css等。

jquery将所有的方法封装在jquery中，而$是一个合法的变量名，也是jquery的别名。$本质上是一个函数，函数也是对象，所以除了直接调用外，$还有许多属性。
如果$属性被占用了，那我们就让jquery将$变量交出来，继续使用jquery
$; // jQuery(selector, context)
jQuery.noConflict();
$; // undefined
jQuery; // jQuery(selector, context)