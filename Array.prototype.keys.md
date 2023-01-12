
## Array.prototype.keys()


> keys() 方法返回一个包含数组中每个索引键(::包含那些没有对应元素的索引::)的 Array Iterator 对象。

```js
console.log('密集数组', [...[1, 2, 3].keys()]);

console.log('稀疏数组', [...(Array(10).keys())]);
```