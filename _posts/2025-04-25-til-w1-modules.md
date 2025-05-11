---
title: 모듈 시스템
date: 2025-04-25
layout: single
---
<h1 style="text-align: center;"></h1>


## ✅ 모듈이란?

- 하나의 자바스크립트 파일은 하나의 모듈 이다.
- 변수, 함수, 클래스 등을 **외부 파일에서 불러오거나 내보낼 수 있게** 하며,
- 코드 재사용, 충돌 방지, 파일 역할 분리를 가능하게 해준다.

---

## ✅ 모듈 시스템이 왜 필요할까?

- 전역 변수 충돌 문제를 방지하고,
- 코드 구조를 기능별로 나누어 **유지보수와 가독성**을 높입니다.
- 필요한 기능만 골라 불러올 수 있어서 **성능 최적화**에도 도움이 됩니다.

---
### 📁 자주 사용되는 모듈의 종류는 크게 두가지로 나뉜다.

| 항목         | CommonJS (`require`)         | ES Modules (`import`)      |
|--------------|-------------------------------|-----------------------------|
| 사용 환경     | Node.js                      | 브라우저 + Node.js          |
| 문법         | `require`, `module.exports`   | `import`, `export`          |
| 실행 시점     | 런타임(동기)                 | 파싱 시점(비동기)           |
| 호환성       | 기존 코드와 잘 호환됨        | 최신 개발 방식과 호환       |

---

### 🔍 CommonJS (CJS) – Node.js에서 주로 사용

```js

// math.js
const add = (a, b) => a + b;
module.exports = { add };

// main.js
const math = require('./math');
console.log(math.add(2, 3));

```
* **math.js**에서 add 함수를 **module.exports** 로 내보내고, <br>
  **main.js**에서 **require()** 를 통해 불러와 사용하는 구조

