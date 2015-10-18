this隐式绑定

例1：

```javascript
var me = {
	a: 3,
	show:show
};
function show(){
	console.log(this.a);
}
me.show(); //this绑定到me上，输出3
```

例2：
如果将me.show赋值给一个变量，再调用：

```javascript
var show1 = me.show;
show1(); //undefine,和上例完全不同！！
```

例3：
同样，作为回调函数：

```javascript
setTimeout(me.show, 1000); //undefine,参数传递其实就是一种赋值，结果和例2一样
```

例4：
例3的解决方法：

```javascript
setTimeout(function(){me.show();}, 1000); //3,传递了一个匿名函数直接调用me.show()，结果和例1一样
```
