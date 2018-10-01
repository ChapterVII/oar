# oar-string
[TOC]
## 字符串比较
#### 常用
比较运算符： 对于数字已数字的方式工作，对于字符串以词法的方式工作
```js
console.log('banana' > 'apple') // true: 字母表中排在后面的大
console.log('a' > 'A') // true: 小写字母比大写字母大
```
#### 不常用
> localeCompare()  

如果两个字符串相同，返回0，如果参数字符串从词法上比被比较字符串大，则返回-1，否则返回1
```js
console.log('apple'.localeCompare('banana')) // -1
```
## 查找子字符串
#### 常用
> indexOf()
#### 不常用
> lastIndexOf()  

返回子字符串最后出现的索引位置
```js
const str = 'my music, good music'
const subStr = 'music'
console.log(str.indexOf(subStr)) // 3:存在则返回索引
console.log(str.indexOf('voice')) // -1: 不存在返回-1
console.log(str.indexOf(subStr, 9)) // 15, 第二个可选参数表示从该位置开始向后查找

console.log(str.lastIndexOf(subStr)) // 15
// lastIndexOf 的第二个可选参数表示在该位置的前面子字符串最后一次出现的索引
console.log(str.lastIndexOf(subStr, 10)) // 3
console.log(str.lastIndexOf(subStr, 2)) // -1
```
## 提取子字符串
#### 常用
> substring(start, stop)  

知道子字符串所在的首尾位置时使用, stop参数可选，若不传，则提取到结尾位置，提取的为start到stop + 1 之间的所有字符，包括start,不包括stop

> substr(start, length)  

知道子字符串所在的首位和长度时使用, length参数可选，若不传，则提取到结尾位置，提取的为start(包括start)开始的length个字符
## 检查存在且非空的字符串
#### 最准确
` typeof str !== undefined && type of str.valueof() == 'string' && str.length > 0 `
#### 关注点
如果不用valueOf(): 如果变量是一个String对象，而不是一个直接量，typeof将返回一个object数据类型而不是string
> valueOf  

对于所有js对象都可用，返回其基本值
## 分隔字符串
> split(separator,howmany)

第一个参数为分隔符，常见如, 第二个参数可选，表示进行分隔的次数
#### 特殊用法
1. 如果想要根据每个字符来分隔一个字符串，指定空字符串('')或("")作为分隔符
2. 也可以使用一个正则表达式作为参数进行分隔
```js
const str1 = 'apple, banana, egg, orange'
console.log(str1.split(',', 2)) // ['apple', 'banana']
const str2 = str1.split(',')[0] // 'apple'
console.log(str2.split('')) // ['a', 'p', 'p', 'l', 'e']
```
## 去除空白
#### 常用
> trim() 

字符串两端的空白都会被去除掉
#### 不常用
> trimLeft: 去除字符串左边的空白  
trimRight: 去除字符串右边的空白




