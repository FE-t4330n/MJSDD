**[예제 20-01]**

```js
function foo() {
  x = 10;
}
foo();

console.log(x); // ?
```

**[예제 20-02]**

```js
"use strict";

function foo() {
  x = 10; // ReferenceError: x is not defined
}
foo();
```

**[예제 20-03]**

```js
function foo() {
  "use strict";

  x = 10; // ReferenceError: x is not defined
}
foo();
```

**[예제 20-04]**

```js
function foo() {
  x = 10; // 에러를 발생시키지 않는다.
  ("use strict");
}
foo();
```
