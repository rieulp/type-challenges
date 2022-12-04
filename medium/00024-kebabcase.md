<h1>KebabCase <img src="https://img.shields.io/badge/-medium-d9901a" alt="medium"/> <img src="https://img.shields.io/badge/-%23template--literal-999" alt="#template-literal"/></h1><p><a href="https://tsch.js.org/612/play" target="_blank"><img src="https://img.shields.io/badge/-Take%20the%20Challenge-3178c6?logo=typescript&logoColor=white" alt="Take the Challenge"/></a>

Replace the `camelCase` or `PascalCase` string with `kebab-case`.

`FooBarBaz` -> `foo-bar-baz`

For example

```ts
type FooBarBaz = KebabCase<"FooBarBaz">;
const foobarbaz: FooBarBaz = "foo-bar-baz";

type DoNothing = KebabCase<"do-nothing">;
const doNothing: DoNothing = "do-nothing";
```

## 정답

<a href="https://tsch.js.org/612/solutions" target="_blank"><img src="https://img.shields.io/badge/-Check%20out%20Solutions-de5a77?logo=awesome-lists&logoColor=white" alt="Check out Solutions"/></a>

```ts
type KebabCase<S extends string> = S extends `${infer A}${infer B}`
  ? B extends Uncapitalize<B>
    ? `${Uncapitalize<A>}${KebabCase<B>}`
    : `${Uncapitalize<A>}-${KebabCase<B>}`
  : S;
```
