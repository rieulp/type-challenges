<h1>String to Union <img src="https://img.shields.io/badge/-medium-d9901a" alt="medium"/> <img src="https://img.shields.io/badge/-%23union-999" alt="#union"/> <img src="https://img.shields.io/badge/-%23string-999" alt="#string"/></h1><p><a href="https://tsch.js.org/531/play" target="_blank"><img src="https://img.shields.io/badge/-Take%20the%20Challenge-3178c6?logo=typescript&logoColor=white" alt="Take the Challenge"/></a></p>
Implement the String to Union type. Type take string argument. The output should be a union of input letters

For example

```ts
type Test = "123";
type Result = StringToUnion<Test>; // expected to be "1" | "2" | "3"
```

## 정답

<a href="https://tsch.js.org/531/solutions" target="_blank"><img src="https://img.shields.io/badge/-Check%20out%20Solutions-de5a77?logo=awesome-lists&logoColor=white" alt="Check out Solutions"/></a>

```ts
type StringToUnion<T extends string> = T extends `${infer S}${infer Rest}`
  ? S | StringToUnion<Rest>
  : never;
```
