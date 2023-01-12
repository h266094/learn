## 手写 extends

[参考](https://lxchuan12.gitee.io/js-extend/#%E6%9E%84%E9%80%A0%E5%87%BD%E6%95%B0%E3%80%81%E5%8E%9F%E5%9E%8B%E5%AF%B9%E8%B1%A1%E5%92%8C%E5%AE%9E%E4%BE%8B%E4%B9%8B%E9%97%B4%E7%9A%84%E5%85%B3%E7%B3%BB)

[参考1](https://keenwon.com/1524/https://keenwon.com/1524/)

```js
function Parent(name){
  this.name = name;
}
Parent.sayHello = function(){
  console.log('hello');
}
Parent.prototype.sayName = function(){
  console.log('my name is ' + this.name);
  return this.name;
}

function Child(name, age){
  // 相当于super
  Parent.call(this, name);
  this.age = age;
}

function _inherits(Child, Parent){
  Object.setPrototypeOf(Child.prototype, Parent.prototype);
  Object.setPrototypeOf(Child, Parent);
}

_inherits(Child,  Parent);

const child = new Child('a', 100);

child.sayName();

console.log(Object.getPrototypeOf(Child) === Parent);
```
