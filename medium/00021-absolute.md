<h1>Absolute <img src="https://img.shields.io/badge/-medium-d9901a" alt="medium"/> <img src="https://img.shields.io/badge/-%23math-999" alt="#math"/> <img src="https://img.shields.io/badge/-%23template--literal-999" alt="#template-literal"/></h1><p><a href="https://tsch.js.org/529/play" target="_blank"><img src="https://img.shields.io/badge/-Take%20the%20Challenge-3178c6?logo=typescript&logoColor=white" alt="Take the Challenge"/></a>

Implement the `Absolute` type. A type that take string, number or bigint. The output should be a positive number string

For example

```ts
type Test = -100;
type Result = Absolute<Test>; // expected to be "100"
```

## 정답

<a href="https://tsch.js.org/529/solutions" target="_blank"><img src="https://img.shields.io/badge/-Check%20out%20Solutions-de5a77?logo=awesome-lists&logoColor=white" alt="Check out Solutions"/></a>

```ts
type Absolute<T extends number | string | bigint> = `${T}` extends `-${infer N}`
  ? Absolute<`${N}`>
  : `${T}`;
```
