**[예제 32-01]**

```js
const strObj = new String();
console.log(strObj); // String {length: 0, [[PrimitiveValue]]: ""}
```

**[예제 32-02]**

```js
const strObj = new String("Lee");
console.log(strObj);
// String {0: "L", 1: "e", 2: "e", length: 3, [[PrimitiveValue]]: "Lee"}
```

**[예제 32-03]**

```js
console.log(strObj[0]); // L
```

**[예제 32-04]**

```js
// 문자열은 원시값이므로 변경할 수 없다. 이때 에러가 발생하지 않는다.
strObj[0] = "S";
console.log(strObj); // 'Lee'
```

**[예제 32-05]**

```js
let strObj = new String(123);
console.log(strObj);
// String {0: "1", 1: "2", 2: "3", length: 3, [[PrimitiveValue]]: "123"}

strObj = new String(null);
console.log(strObj);
// String {0: "n", 1: "u", 2: "l", : "l", length: 4, [[PrimitiveValue]]: "null"}
```

**[예제 32-06]**

```js
// 숫자 타입 => 문자열 타입
String(1); // -> "1"
String(NaN); // -> "NaN"
String(Infinity); // -> "Infinity"

// 불리언 타입 => 문자열 타입
String(true); // -> "true"
String(false); // -> "false"
```

**[예제 32-07]**

```js
"Hello".length; // -> 5
"안녕하세요!".length; // -> 6
```
