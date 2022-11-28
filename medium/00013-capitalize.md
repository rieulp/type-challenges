<h1>Capitalize <img src="https://img.shields.io/badge/-%EB%B3%B4%ED%86%B5-d9901a" alt="보통"/> <img src="https://img.shields.io/badge/-%23template--literal-999" alt="#template-literal"/></h1><p><a href="https://tsch.js.org/110/play/ko" target="_blank"><img src="https://img.shields.io/badge/-%EB%8F%84%EC%A0%84%ED%95%98%EA%B8%B0-3178c6?logo=typescript&logoColor=white" alt="도전하기"/></a>

문자열의 첫 글자만 대문자로 바꾸고 나머지는 그대로 놔두는 `Capitalize<T>`를 구현하세요.

예시:

```ts
type capitalized = Capitalize<"hello world">; // expected to be 'Hello world'
```

## 정답

<a href="https://tsch.js.org/110/solutions" target="_blank"><img src="https://img.shields.io/badge/-%EC%A0%95%EB%8B%B5%20%EB%B3%B4%EA%B8%B0-de5a77?logo=awesome-lists&logoColor=white" alt="정답 보기"/></a>

```ts
type MyCapitalize<S extends string> = S extends `${infer First}${infer Tail}`
  ? `${Uppercase<First>}${Tail}`
  : S;
```
