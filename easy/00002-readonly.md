<!--info-header-start--><h1>Readonly <img src="https://img.shields.io/badge/-%EC%89%AC%EC%9B%80-7aad0c" alt="쉬움"/> <img src="https://img.shields.io/badge/-%23built--in-999" alt="#built-in"/> <img src="https://img.shields.io/badge/-%23readonly-999" alt="#readonly"/> <img src="https://img.shields.io/badge/-%23object--keys-999" alt="#object-keys"/></h1>
<p><a href="https://tsch.js.org/7/play/ko" target="_blank"><img src="https://img.shields.io/badge/-%EB%8F%84%EC%A0%84%ED%95%98%EA%B8%B0-3178c6?logo=typescript&logoColor=white" alt="도전하기"/></a><!--info-header-end-->

`T`의 모든 프로퍼티를 읽기 전용(재할당 불가)으로 바꾸는 내장 제네릭 `Readonly<T>`를 이를 사용하지 않고 구현하세요.

예시:

```ts
interface Todo {
  title: string
  description: string
}

const todo: MyReadonly<Todo> = {
  title: "Hey",
  description: "foobar"
}

todo.title = "Hello" // Error: cannot reassign a readonly property
todo.description = "barFoo" // Error: cannot reassign a readonly property
```

## 정답
<a href="https://han.gl/cKkkA" target="_blank"><img src="https://img.shields.io/badge/-%EC%A0%95%EB%8B%B5%20%EB%B3%B4%EA%B8%B0-de5a77?logo=awesome-lists&logoColor=white" alt="정답 보기"/></a>
```ts
type MyReadonly<T> = {
  readonly [key in keyof T]:T[key]
}
```
