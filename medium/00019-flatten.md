<h1>Flatten <img src="https://img.shields.io/badge/-%EB%B3%B4%ED%86%B5-d9901a" alt="보통"/> <img src="https://img.shields.io/badge/-%23array-999" alt="#array"/></h1><p><a href="https://tsch.js.org/459/play/ko" target="_blank"><img src="https://img.shields.io/badge/-%EB%8F%84%EC%A0%84%ED%95%98%EA%B8%B0-3178c6?logo=typescript&logoColor=white" alt="도전하기"/></a>

주어진 배열을 플랫한 배열 타입으로 바꾸는 Flatten 타입을 구현하세요.

예시:

```ts
type flatten = Flatten<[1, 2, [3, 4], [[[5]]]]>; // [1, 2, 3, 4, 5]
```

## 정답

<a href="https://tsch.js.org/459/solutions" target="_blank"><img src="https://img.shields.io/badge/-%EC%A0%95%EB%8B%B5%20%EB%B3%B4%EA%B8%B0-de5a77?logo=awesome-lists&logoColor=white" alt="정답 보기"/></a>

```ts
type Flatten<T extends any[]> = T extends [infer U, ...infer R]
  ? U extends any[]
    ? Flatten<[...U, ...R]>
    : [U, ...Flatten<[...R]>]
  : T;
```
