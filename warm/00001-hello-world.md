<!--info-header-start-->
<h1>Hello World <img src="https://img.shields.io/badge/-%EC%9B%8C%EB%B0%8D%EC%97%85-teal" alt="워밍업"/> </h1>

<p><a href="https://tsch.js.org/13/play/ko" target="_blank"><img src="https://img.shields.io/badge/-%EB%8F%84%EC%A0%84%ED%95%98%EA%B8%B0-3178c6?logo=typescript&logoColor=white" alt="도전하기"/></a>
<!--info-header-end-->

Hello, World!

Type Challenges에서는 타입 단언(assertion)을 하기 위해 자체적인 타입 시스템을 사용합니다.

이 과제에서는, 아래의 코드를 변경해서 테스트 코드를 통과하세요. (타입 체크 에러 없음).

```ts
// string이 되어야 합니다.
type HelloWorld = any
```

```ts
// 아래의 테스트가 통과하도록 만드세요.
type test = Expect<Equal<HelloWorld, string>>
```

## 정답
  <a href="[https://tsch.js.org/13/solutions](https://www.typescriptlang.org/play?#code/PQKgUABBCMDMEFoIAkCmAbdB7CB1LATugCaSIIWVkBGAnhAIIB2ALgBZZP0BiArhAAoAAgENWAM14BKCAGJAM2OBYHsCjoxDJlZmiIAnJwBzd6qGkxYANHkIkAhAYgAVWgAdUEAMJsRmVEwDmqAM6AC6OAOIOAKU0QgAMLgKHjEIAXTYAdowIifn6oBCwAlpxSgCLjEIAaq4AMdRCAIOOALqsQgAnjgC0zgIATgB7jEdGAO0OAJUOAOou5gDUDgJVjgJargBNNgCdNAHQ2gC7jEIA-NYA4E8EhZoAio4AZ7YAa4xCAKvOAOy2APp0QgAM9gL01pUEQgDKLLYAdSxs7EICti5N5gByDgCljw4JREFWANgsQAYA37RBAGOjgBlxqSjKBkAAG0JYfjIwGAED8LAI6R8E0AGC2AFtHAD6jEAGIzILEcziM2HwRGIEAAvBAxLQodCbNDIbD4YjlmtzhdAAA1dwegBHmwC6HRBADOdmxe4IgxKc0v8LBpEAAogAPJwAYxYAB4lQBHXgeLVkrAUkhmZGonwAPitjMhzNsIgA1s52M43B50F5fJCIIAQnsAPUu5QAuC4BazuOG0AlK25JqARPGns9LCgRA4HPRkCJ1U60d5rBCoFaIABxdIsZC8ajBCCAF56CgAuCBsFgsBx+OsI2HqtjDABWfmGhG8wDgwCdWDAIGAYGnoAgAH0F4ul4uIIAb0YKAWuEEigFIO+fLg9ziCT6cy0kYckWKm0i05iAIiCoNWoTWoKksHDUZwiJEonPTsBZ0PA8zkuCBAAB5sYWn3YCVxPdIAFsHEIBUzwgABvZV9Q8MxVQ1FgzAAOSwFhmHoABfCBxAILAEIgAByIQzwQLtPW9fxgF4DJ0D8ejTxJCB1SSfxFQAbTIPCX21YjSK4I0LxNK8bRMCTn01HVsPQeTjFNYhzT-a0rRUgBdADAJAGDYKPQZgViQARmss2DjynUAyELQBUCcAV6aIEAV5rAAJxwoGybFs2w7Pwu17ftB2HWBgDEPwAHdUlHccCwgLya3rRtm1bdtgE7bs+wHAghxHPwsHQLjMiYOE0sGQAPTogXRpkAE5agpy0L8vCwqopKlKJynMAgA)" target="_blank"><img src="https://img.shields.io/badge/-%EC%A0%95%EB%8B%B5%20%EB%B3%B4%EA%B8%B0-de5a77?logo=awesome-lists&logoColor=white" alt="정답 보기"/></a>
```ts
  // string이 되어야 합니다.
  type HelloWord = string
```
