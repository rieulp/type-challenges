<!--info-header-start--><h1>Deep Readonly <img src="https://img.shields.io/badge/-%EB%B3%B4%ED%86%B5-d9901a" alt="보통"/> <img src="https://img.shields.io/badge/-%23readonly-999" alt="#readonly"/> <img src="https://img.shields.io/badge/-%23object--keys-999" alt="#object-keys"/> <img src="https://img.shields.io/badge/-%23deep-999" alt="#deep"/></h1><p><a href="https://tsch.js.org/9/play/ko" target="_blank"><img src="https://img.shields.io/badge/-%EB%8F%84%EC%A0%84%ED%95%98%EA%B8%B0-3178c6?logo=typescript&logoColor=white" alt="도전하기"/></a>

객체의 프로퍼티와 모든 하위 객체를 재귀적으로 읽기 전용으로 설정하는 제네릭 `DeepReadonly<T>`를 구현하세요.

이 챌린지에서는 타입 파라미터 `T`를 객체 타입으로 제한하고 있습니다. 객체뿐만 아니라 배열, 함수, 클래스 등 가능한 다양한 형태의 타입 파라미터를 사용하도록 도전해 보세요.

예시:

```ts
type X = {
  x: {
    a: 1;
    b: "hi";
  };
  y: "hey";
};

type Expected = {
  readonly x: {
    readonly a: 1;
    readonly b: "hi";
  };
  readonly y: "hey";
};

type Todo = DeepReadonly<X>; // should be same as `Expected`
```

## 정답

<a href="https://tsch.js.org/9/solutions" target="_blank"><img src="https://img.shields.io/badge/-%EC%A0%95%EB%8B%B5%20%EB%B3%B4%EA%B8%B0-de5a77?logo=awesome-lists&logoColor=white" alt="정답 보기"/></a>

```ts
type DeepReadonly<T> = T extends Object
  ? T extends Promise<any> | Function
    ? T
    : { readonly [key in keyof T]: DeepReadonly<T[key]> }
  : T;
```
