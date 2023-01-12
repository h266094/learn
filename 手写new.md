
## 手写new

```js
const _new = function (ctor) {
  if (typeof ctor !== 'function') {
    throw 'ctor must be a function'
  }

  const obj = Object.create(ctor.prototype);
  const args = [].slice.call(arguments, 1);
  const result = ctor.apply(obj, args);

  const isObject = typeof result === 'object' && result !== null;
  const isFunction = typeof result === 'function';

  if (isObject || isFunction) {
    return result;
  }

  return obj;
}


function Student(name, age) {
  this.name = name;
  this.age = age;

  return this;
}

Student.prototype.doSth = function () {
  console.log(this.name, this.age);
};


const student1 = _new(Student, '若', 18);


console.log(student1);
student1.doSth();

console.log(student1.__proto__ === Student.prototype); // true
```