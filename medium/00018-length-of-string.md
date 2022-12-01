<h1>Length of String <img src="https://img.shields.io/badge/-%EB%B3%B4%ED%86%B5-d9901a" alt="보통"/> <img src="https://img.shields.io/badge/-%23template--literal-999" alt="#template-literal"/></h1><p><a href="https://tsch.js.org/298/play/ko" target="_blank"><img src="https://img.shields.io/badge/-%EB%8F%84%EC%A0%84%ED%95%98%EA%B8%B0-3178c6?logo=typescript&logoColor=white" alt="도전하기"/></a>

`String#length`처럼 동작하는 문자열 리터럴의 길이를 구하세요.

## 정답

<a href="https://tsch.js.org/298/solutions" target="_blank"><img src="https://img.shields.io/badge/-%EC%A0%95%EB%8B%B5%20%EB%B3%B4%EA%B8%B0-de5a77?logo=awesome-lists&logoColor=white" alt="정답 보기"/></a>

```ts
type LengthOfString<
  S extends string,
  K extends string[] = []
> = S extends `${string}${infer R}`
  ? LengthOfString<R, [...K, string]>
  : K["length"];
```
