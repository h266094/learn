## 手写Object.create()

```js
function _create(paramProto){
  const isObject = (typeof paramProto === 'object') || (typeof paramProto === 'function');
  const isUndefined = typeof paramProto === 'undefined';
  if (isUndefined || !isObject){
    throw new TypeError('Object prototype may only be an Object or null: ' + paramProto)
  }

  function F() { }
  F.prototype = paramProto;
  return new F();
}

```