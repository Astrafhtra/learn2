类型 typeof
复杂类型就是 object
Array 是可遍历的对象
Function 是可运行的对象
JSON object字面量是可枚举的对象 for（key in）
typeof  半吊子 typeof []没办法和json区分开来
有一个方法可以区分Array JSON Object


1. 用对象字面量来做面对向对象，区别于原型式的 它没有被实例化的需要 Type 将在程序中的做类型检测
var Type = {}; 组织代码
2. for 来一次性的加完 同步异步的问题 闭包来将type的作用域封闭起来，立即执行函数 同步执行，类型检测函数的定义，因为函数嵌套，形成了闭包，当函数再被调用时（异步） ，找到定义时刻的type
3. Object.prototype.String.call(obj) 
  Object? 祖先，顶级对象 函数才有prototype ，原型上有toString方法，解决type的尴尬， "[ object,object]"
  [object,Array] 方法执行的方式被改变 Object.prototype.String.call(obj) 