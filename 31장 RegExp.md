**[예제 31-01]**

```js
// 사용자로부터 입력받은 휴대폰 전화번호
const tel = "010-1234-567팔";

// 정규 표현식 리터럴로 휴대폰 전화번호 패턴을 정의한다.
const regExp = /^\d{3}-\d{4}-\d{4}$/;

// tel이 휴대폰 전화번호 패턴에 매칭하는지 테스트(확인)한다.
regExp.test(tel); // -> false
```

**[예제 31-02]**

```js
const target = "Is this all there is?";

// 패턴: is
// 플래그: i => 대소문자를 구별하지 않고 검색한다.
const regexp = /is/i;

// test 메서드는 target 문자열에 대해 정규표현식 regexp의 패턴을 검색하여 매칭 결과를 불리언 값으로 반환한다.
regexp.test(target); // -> true
```

**[예제 31-03]**

```js
const target = "Is this all there is?";

const regexp = new RegExp(/is/i); // ES6
// const regexp = new RegExp(/is/, 'i');
// const regexp = new RegExp('is', 'i');

regexp.test(target); // -> true
```

**[예제 31-04]**

```js
const count = (str, char) => (str.match(new RegExp(char, "gi")) ?? []).length;

count("Is this all there is?", "is"); // -> 3
count("Is this all there is?", "xx"); // -> 0
```

**[예제 31-05]**

```js
const target = "Is this all there is?";
const regExp = /is/;

regExp.exec(target); // -> ["is", index: 5, input: "Is this all there is?", groups: undefined]
```

**[예제 31-06]**

```js
const target = "Is this all there is?";
const regExp = /is/;

regExp.test(target); // -> true
```

**[예제 31-07]**

```js
const target = "Is this all there is?";
const regExp = /is/;

target.match(regExp); // -> ["is", index: 5, input: "Is this all there is?", groups: undefined]
```

**[예제 31-08]**

```js
const target = "Is this all there is?";
const regExp = /is/g;

target.match(regExp); // -> ["is", "is"]
```
