<h1>Tuple to Union <img src="https://img.shields.io/badge/-%EB%B3%B4%ED%86%B5-d9901a" alt="보통"/> <img src="https://img.shields.io/badge/-%23infer-999" alt="#infer"/> <img src="https://img.shields.io/badge/-%23tuple-999" alt="#tuple"/> <img src="https://img.shields.io/badge/-%23union-999" alt="#union"/></h1><p><a href="https://tsch.js.org/10/play/ko" target="_blank"><img src="https://img.shields.io/badge/-%EB%8F%84%EC%A0%84%ED%95%98%EA%B8%B0-3178c6?logo=typescript&logoColor=white" alt="도전하기"/></a>

튜플 값으로 유니온 타입을 생성하는 제네릭 `TupleToUnion<T>`를 구현하세요.

예시:

```ts
type Arr = ["1", "2", "3"];

type Test = TupleToUnion<Arr>; // expected to be '1' | '2' | '3'
```

## 정답

<a href="https://tsch.js.org/10/solutions" target="_blank"><img src="https://img.shields.io/badge/-%EC%A0%95%EB%8B%B5%20%EB%B3%B4%EA%B8%B0-de5a77?logo=awesome-lists&logoColor=white" alt="정답 보기"/></a>

```ts
// 방법 1
type TupleToUnion<T extends Array<any>> = T extends Array<infer U> ? U : never;
// 방법 2
type TupleToUnion<T extends Array<unknown>> = T[number];
```
