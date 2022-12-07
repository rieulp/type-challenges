<h1>Drop Char <img src="https://img.shields.io/badge/-medium-d9901a" alt="medium"/> <img src="https://img.shields.io/badge/-%23template--literal-999" alt="#template-literal"/> <img src="https://img.shields.io/badge/-%23infer-999" alt="#infer"/></h1><p><a href="https://tsch.js.org/2070/play" target="_blank"><img src="https://img.shields.io/badge/-Take%20the%20Challenge-3178c6?logo=typescript&logoColor=white" alt="Take the Challenge"/></a>

Drop a specified char from a string.

For example:

```ts
type Butterfly = DropChar<" b u t t e r f l y ! ", " ">; // 'butterfly!'
```

## 정답

<a href="https://tsch.js.org/2070/solutions" target="_blank"><img src="https://img.shields.io/badge/-Check%20out%20Solutions-de5a77?logo=awesome-lists&logoColor=white" alt="Check out Solutions"/></a>

```ts
type DropChar<S, C> = S extends `${infer Char}${infer Rest}`
  ? Char extends C
    ? DropChar<Rest, C>
    : `${Char}${DropChar<Rest, C>}`
  : "";
```
