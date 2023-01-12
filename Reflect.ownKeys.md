## Reflect.ownKeys()


> Reflect.ownKeys() 返回 **自身所有的属性名(包含不可枚举)**，还包括 Symbol 值作为名称的属性。

```js

const symbol = Symbol('other');

const obj = {a: 1, b: 2, [symbol]: 'other', d: () => console.log(1)};

Object.prototype.wwt = 100;

Object.defineProperty(obj, 'c', {
  value: 3,
  //设置不可枚举
  enumerable: false
})

console.log(obj);
console.log(Object.getOwnPropertyNames(obj));
console.log(Reflect.ownKeys(obj));

```