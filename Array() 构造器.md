## Array() 构造器


> Array() 可以调用或不调用 new。两者都会创建一个新的 Array 实例。

```js
console.log('new Array', new Array(1,2,3,4)); 
console.log('Array', new Array(1,2,3,4)); 
```


Array 构造器会根据给定的元素创建一个 JavaScript 数组，但是当仅有一个参数且为数字时，则创建::指定长度的稀疏空数组::。


```js
console.log('Array 多个参数', Array(1,2,3, 'a')); 
console.log('Array 参数一个且为数组', Array(10));

```
