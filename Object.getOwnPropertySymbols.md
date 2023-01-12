
## Object.getOwnPropertySymbols

> Object.getOwnPropertySymbols() 返回对象 **所有Symbol属性**的数组。

```js

const obj = {};

const a = Symbol("a");
const b = Symbol.for("b");
const c = Symbol("c");

obj[a] = "localSymbol";
obj[b] = "globalSymbol";


Object.defineProperty(obj, c, {
  value: 100,
  enumerable: false
})

const objectSymbols = Object.getOwnPropertySymbols(obj);

console.log(objectSymbols);

```