# javascript中判断取值

经常做三元运算的时候，如果条件成立，则取自身，否则取另一个值，这时候可以这样写

```javascript
var a = "a"
console.log(a&&'-'); //'-'
console.log(a||'-'); //a
```
## 知识点

> * &&运算符规则：a&&b，如果 a 为true，直接返回 b；如果 a 为false 那么直接返回 a。

> * || 运算符规则：a || b，如果 a 为true，直接返回 a；如果 a 为false 那么直接返回 b。