## Object.setPrototypeOf()

> Object.setPrototypeOf() 方法设置一个指定的对象的原型（即，内部 [[Prototype]] 属性）到另一个对象或 null。


```js
console.log(Object.create(null));
console.log(Object.setPrototypeOf({}, null));
```

```js
Object.setPrototypeOf = Object.setPrototypeOf || function (obj, proto) {
  obj.__proto__ = proto;
  return obj;
}
```