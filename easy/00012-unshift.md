<h1>Unshift <img src="https://img.shields.io/badge/-%EC%89%AC%EC%9B%80-7aad0c" alt="쉬움"/> <img src="https://img.shields.io/badge/-%23array-999" alt="#array"/></h1><p><a href="https://tsch.js.org/3060/play/ko" target="_blank"><img src="https://img.shields.io/badge/-%EB%8F%84%EC%A0%84%ED%95%98%EA%B8%B0-3178c6?logo=typescript&logoColor=white" alt="도전하기"/></a>

`Array.unshift`의 타입 버전을 구현하세요.

예시:

```typescript
type Result = Unshift<[1, 2], 0>; // [0, 1, 2,]
```

## 정답

<a href="https://tinyurl.com/2nkqj96v" target="_blank"><img src="https://img.shields.io/badge/-%EC%A0%95%EB%8B%B5%20%EB%B3%B4%EA%B8%B0-de5a77?logo=awesome-lists&logoColor=white" alt="정답 보기"/></a>

```ts
type Unshift<T extends unknown[], U> = [U, ...T];
```
