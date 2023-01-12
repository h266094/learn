## Object.keys()

> Object.keys() 方法会返回给定对象的**自身可枚举属性**组成的数组，不包括 Symbol 值作为名称的属性。

```js
const symbol = Symbol('other');

const obj = {a: 1, b: 2, [symbol]: 'other', d: () => console.log(1)};

Object.prototype.wwt = 100;

Object.defineProperty(obj, 'c', {
  value: 3,
  //设置不可枚举
  enumerable: false
})

console.log(obj, Object.keys(obj));
```