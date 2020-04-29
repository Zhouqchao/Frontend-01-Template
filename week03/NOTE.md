# 总结

## 基本对象

基本对象是定义或使用其他对象的基础。基本对象包括一般对象、函数对象和错误对象。

## 一般对象、函数对象

Object
Function
Boolean
Symbol

## 错误对象

错误对象是一种特殊的基本对象。它们拥有基本的 Error 类型，同时也有多种具体的错误类型。

Error（通过 Error 的构造器可以创建一个错误对象。当运行时错误产生时，Error 的实例对象会被抛出。Error 对象也可用于用户自定义的异常的基础对象。）
new Error([message[, fileName[,lineNumber]]])
AggregateError
EvalError
RangeError(标明一个错误，当一个值不在其所允许的范围或者集合中。)
ReferenceError(代表当一个不存在的变量被引用时发生的错误。)
SyntaxError(对象代表尝试解析语法上不合法的代码的错误。)
TypeError(对象用来表示值的类型非预期类型时发生的错误。
语法)

URLError(URIError 对象用来表示以一种错误的方式使用全局 URI 处理函数而产生的错误。)

## 数字和日期对象

用来表示数字、日期和执行数学计算的对象。

Number
BigInt(它提供了一种方法来表示大于 253 - 1 的整数。这原本是 Javascript 中可以用 Number 表示的最大数字。BigInt 可以表示任意大的整数。)
Math
Date

## 字符串

用来表示和操作字符串的对象。

String
RegExp
可索引的集合对象
表示按照索引值来排序的数据集合，包括数组和类型数组，以及类数组结构的对象。

## TypedArray

Int8Array
Uint8Array
Uint8ClampedArray
Int16Array
Uint16Array
Int32Array
Uint32Array
Float32Array
Float64Array
BigInt64Array
BigUint64Array

## 使用键的集合对象

这些集合对象在存储数据时会使用到键，包括可迭代的 Map 和 Set，支持按照插入顺序来迭代元素。

Map
Set
WeakMap
WeakSet
