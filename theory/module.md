# 📌 모둘


## ✅ module.exports

__test.js__
```ts
const template = {
  a : 'a',
  b : 'b',
}
module.exports = template;

// or

module.exports = {
  a : 'a',
  b : 'b'
}
```

__abc.js__

```ts
const template = require('test.js');
console.log(template.a); // a
```