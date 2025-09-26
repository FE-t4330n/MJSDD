**[예제 28-01]**

```js
const numObj = new Number();
console.log(numObj); // Number {[[PrimitiveValue]]: 0}
```

**[예제 28-02]**

```js
const numObj = new Number(10);
console.log(numObj); // Number {[[PrimitiveValue]]: 10}
```

**[예제 28-03]**

```js
let numObj = new Number("10");
console.log(numObj); // Number {[[PrimitiveValue]]: 10}

numObj = new Number("Hello");
console.log(numObj); // Number {[[PrimitiveValue]]: NaN}
```

**[예제 28-04]**

```js
// 문자열 타입 => 숫자 타입
Number("0"); // -> 0
Number("-1"); // -> -1
Number("10.53"); // -> 10.53

// 불리언 타입 => 숫자 타입
Number(true); // -> 1
Number(false); // -> 0
```

**[예제 28-05]**

```js
0.1 + 0.2; // -> 0.30000000000000004
0.1 + 0.2 === 0.3; // -> false
```

**[예제 28-06]**

```js
function isEqual(a, b) {
  // a와 b를 뺀 값의 절대값이 Number.EPSILON보다 작으면 같은 수로 인정한다.
  return Math.abs(a - b) < Number.EPSILON;
}

isEqual(0.1 + 0.2, 0.3); // -> true
```

**[예제 28-07]**

```js
Number.MAX_VALUE; // -> 1.7976931348623157e+308
Infinity > Number.MAX_VALUE; // -> true
```

**[예제 28-08]**

```js
Number.MIN_VALUE; // -> 5e-324
Number.MIN_VALUE > 0; // -> true
```

**[예제 28-09]**

```js
Number.MAX_SAFE_INTEGER; // -> 9007199254740991
```

**[예제 28-10]**

```js
Number.MIN_SAFE_INTEGER; // -> -9007199254740991
```

**[예제 28-11]**

```js
Number.POSITIVE_INFINITY; // -> Infinity
```

**[예제 28-12]**

```js
Number.NEGATIVE_INFINITY; // -> -Infinity
```

**[예제 28-13]**

```js
Number.NaN; // -> NaN
```
