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

**[예제 20-05]**

```html
<!DOCTYPE html>
<html>
  <body>
    <script>
      "use strict";
    </script>
    <script>
      x = 1; // 에러가 발생하지 않는다.
      console.log(x); // 1
    </script>
    <script>
      "use strict";

      y = 1; // ReferenceError: y is not defined
      console.log(y);
    </script>
  </body>
</html>
```

**[예제 20-06]**

```js
// 즉시 실행 함수의 선두에 strict mode 적용
(function () {
  "use strict";

  // Do something...
})();
```
