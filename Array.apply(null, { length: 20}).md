
## Array.apply(null, { length: 20})

```
// 1 熟悉一点: {length: 2} 作为Array.apply 第二个参数等同于[undefined, undefined] 作为Array.apply第二个参数 
Array.apply(null, [undefined, undefined]); 

// 2 再熟悉一点：apply方法的执行结果 Array(undefined, undefined); 

// 3 再再熟悉一点：Array方法直接调用和new方式调用等价 new Array(undefined, undefined); 

```