<h1>Append Argument <img src="https://img.shields.io/badge/-%EB%B3%B4%ED%86%B5-d9901a" alt="보통"/> <img src="https://img.shields.io/badge/-%23arguments-999" alt="#arguments"/></h1>
<p><a href="https://tsch.js.org/191/play/ko" target="_blank"><img src="https://img.shields.io/badge/-%EB%8F%84%EC%A0%84%ED%95%98%EA%B8%B0-3178c6?logo=typescript&logoColor=white" alt="도전하기"/></a>

함수 타입 `Fn`과 어떤 타입 `A`가 주어질 때 `Fn`의 인수와 `A`를 마지막 인수로 받는 `Fn`과 동일한 함수 유형인 `G`를 생성하세요.

예시 :

```typescript
type Fn = (a: number, b: string) => number;

type Result = AppendArgument<Fn, boolean>;
// 기대되는 결과는 (a: number, b: string, x: boolean) => number 입니다.
```

> 이 문제는 [@maciejsikora](https://github.com/maciejsikora)가 작성한 [원문 글](https://dev.to/macsikora/advanced-typescript-exercises-question-4-495c)에서 발췌했습니다.

## 정답

<a href="https://tsch.js.org/191/solutions" target="_blank"><img src="https://img.shields.io/badge/-%EC%A0%95%EB%8B%B5%20%EB%B3%B4%EA%B8%B0-de5a77?logo=awesome-lists&logoColor=white" alt="정답 보기"/></a>

```ts
// built-in 사용
type AppendArgument<Fn extends (...args: any) => any, A> = (
  ...args: [...Parameters<Fn>, A]
) => ReturnType<Fn>;
// 사용 X
type AppendArgument<Fn extends (...args: any) => any, A> = Fn extends (
  ...args: infer Args
) => infer R
  ? (...args: [...Args, A]) => R
  : never;
```
