<h1>IsUnion <img src="https://img.shields.io/badge/-medium-d9901a" alt="medium"/> <img src="https://img.shields.io/badge/-%23union-999" alt="#union"/></h1><p><a href="https://tsch.js.org/1097/play" target="_blank"><img src="https://img.shields.io/badge/-Take%20the%20Challenge-3178c6?logo=typescript&logoColor=white" alt="Take the Challenge"/></a> </p>

Implement a type `IsUnion`, which takes an input type `T` and returns whether `T` resolves to a union type.

For example:

```ts
type case1 = IsUnion<string>; // false
type case2 = IsUnion<string | number>; // true
type case3 = IsUnion<[string | number]>; // false
```

## 정답

<a href="https://tsch.js.org/1097/solutions" target="_blank"><img src="https://img.shields.io/badge/-Check%20out%20Solutions-de5a77?logo=awesome-lists&logoColor=white" alt="Check out Solutions"/></a>

```ts
type IsUnion<T, B = T> = [T] extends [never]
  ? false
  : T extends B
  ? [B] extends [T]
    ? false
    : true
  : never;
```
