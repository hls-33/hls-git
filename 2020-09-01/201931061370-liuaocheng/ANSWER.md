1、javascript原始值类型有哪些（ES5）
	js中有以下五种原始数据类型
	Undefined
	Boolean
	String
	Null
	Number
	还有三种引用数据类型
	Object  
	Array
	Function
	
	
2、为什么 0.1 + 0.2 !== 0.3
	因为在js中并未定义不同类型的的数字数据类型，所有数字都是以64位浮点数形式储存。
	由于浮点数是不准确的（其中的原理主要是因为计算机在储存数值时需要进制转换
	但并不是所有的浮点数在计算机内部都存在误差如0.5就没有误差
	因此在计算0.1+0.2时我们认为的0.1在计算机内部并不是精确的0.1，因此0.1+0.2!==0.3
	所以在使用浮点数时要格外谨慎，尤其时不要直接比较两个浮点数的大小。
	
3、判断数据类型的方法有哪几种
	在js中有3种
	分别为typeof  
	instanceof  
	Object.prototype.toString方法
	
4、null是对象吗，为什么typeof null === 'object'
	null不是对象，null是一种特殊的数据类型。typeof null之所以为object
	是由于在最初的js种只有五种数据类型，000开头代表对象，而null表示为全零
	因此错误的把null表示为object。
	
5、== 与 === 有什么区别？
    ==比较两个值是否相等而===比较他们是否是同一个值如果两个值不是同一类型，严格相等运算符（===）直接返回false，
	而相等运算符（==）会将它们转换成同一个类型，再用严格相等运算符进行比较。
	
6、什么是类数组,如何将类数组转换为数组
	类数组对象其实就是一个常规的对象，只不过它和数组对象十分相似，如arrguments等与数组具有一些相同的属性。
	将类数组转换为数组有多种方式主要根据是哪种类数组而定。
	如类数组arrguments转换为数组有以下两种常用方式
	var args = Array.prototype.slice.call(arguments);
	// 或者
	var args = [];
	for (var i = 0; i < arguments.length; i++) 
	{
		args.push(arguments[i]);
	}
	