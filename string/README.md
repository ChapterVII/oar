# oar-string
## 字符串比较
### 常用
比较运算符： 对于数字已数字的方式工作，对于字符串以词法的方式工作
```js
console.log('banana' > 'apple') // true: 字母表中排在后面的大
console.log('a' > 'A') // true: 小写字母比大写字母大
```
### 不常用
localeCompare方法：如果两个字符串相同，返回0，如果参数字符串从词法上比被比较字符串大，则返回-1，否则返回1
```js
console.log('apple'.localeCompare('banana')) // -1
```
## 查找子字符串
### 常用
indexOf()
### 不常用
lastIndexOf(): 返回子字符串最后出现的索引位置
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




