# ES5


##1. javascript原始值类型有哪些（ES5）

 **原始值**
 

 1. Number (数值)
 2. Boolean (布尔类型)
 3. String (字符串)
 4. Undefined (未定义的)
 5. Null （空）

 

##2.为什么 0.1 + 0.2 !== 0.3
！==是绝对不等于的意思，计算机是用二进制来表示一个浮点数的，所以无法准确的表示一个浮点数，只能无限的逼近它。0.1+0.2与0.3之间存在着一定的误差。故在js中做小数之间的运算会存在着一定的误差。

##3. 判断数据类型的方法有哪几种

 1. typeof 用于判断基本数据类型
 2. instanceof
 3. Object.prototype.toString.call()

##4.null是对象吗，为什么typeof null === 'object'
null不是对象 null是一种数据类型
typeof null == 'object'是一个经典的bug,原理是对象在底层都表示为二进制，在js中二进制前三位为0的话都会被判定为object类型，而null的二进制表示无论哪一位全是0，所以typeof null == 'object'

##5.== 与 === 有什么区别
== 用于检验两个操作数是否相等，允许两个不同数据类型的值相比较 例如 1 == "1" 比较时会转换为同一类型的值，再相比较。
=== 用于检验两个操作数是否严格完全相同，如果两个操作数类型不同 结果也会是不等 例如 console.log(1 === "1");结果是false。

##6.什么是类数组,如何将类数组转换为数组

类数组跟数组很相似，如果一个对象有lenth属性那它就是类数组，比如函数的实参列表arguments就是类数组，它的原始值是Object，argument[0]就是函数的第一个参数（类数组在写法上与数组相同）
将类数组elems转化为数组
Array.prototype.slice.call（elems);




