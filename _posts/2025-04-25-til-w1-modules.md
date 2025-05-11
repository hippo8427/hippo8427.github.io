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
- 코드 구조를 기능별로 나누어 **유지보수와 가독성**을 높인다.
- 필요한 기능만 골라 불러올 수 있어서 **성능 최적화**에도 도움이 된다.

---

<br>
<br>

### 📁 자주 사용되는 모듈의 종류는 크게 두가지로 나뉜다.

| 항목         | CommonJS (`require`)         | ES Modules (`import`)      |
|--------------|-------------------------------|-----------------------------|
| 사용 환경     | Node.js                      | 브라우저 + Node.js          |
| 문법         | `require`, `module.exports`   | `import`, `export`          |
| 실행 시점     | 런타임(동기)                 | 파싱 시점(비동기)           |
| 호환성       | 기존 코드와 잘 호환됨        | 최신 개발 방식과 호환       |

---

### 🔍 CommonJS (CJS) 

```js

// math.js
const add = (a, b) => a + b;
module.exports = { add };

// main.js
const math = require('./math');
console.log(math.add(2, 3));

```
- **math.js**에서 add 함수를 `module.exports` 로 내보내고, <br>
  **main.js**에서 `require()` 를 통해 불러와 사용하는 구조 
- 모듈을 **런타임 시점**에 **동기적**으로 불러오며, 코드가 실행될 때 바로 로딩된다.
- 브라우저 환경에서는 CommonJS가 기본적으로 지원되지 않으며, Node.js 전용이다.

  

---

### 🔍 ES Modules 문법

```js

// math.js
export const add = (a, b) => a + b;


// main.js
import { add } from './math.js';
console.log(add(2, 3));

```
- **math.js**에서 add 함수를 `export`로 내보내고, <br>
  **main.js**에서 `import { add }` 를 사용해 해당 함수를 가져온다. 
- 브라우저와 Node.js 모두에서 사용 가능하며, 문법 자체가 **비동기적인** 현대 표준 모듈 시스템이다.
-  vscode 에서는 packge.json 에 "type": "module" 을 추가해줘야 한다.

<details>
  <summary><strong style="font-size: 1.2em;">🔸 모듈의 동기 vs 비동기 차이 (CommonJS vs ES Modules)</strong></summary>

  <div style="background: #f0f0f0; padding: 1em; " markdown="1">

  | 구분            | CommonJS (CJS)                              | ES Modules (ESM)                                |
|-----------------|----------------------------------------------|-------------------------------------------------|
| **불러오는 시점** | 런타임 시점 (코드 실행 중에 불러옴)         | 파싱 시점 (코드 실행 전에 해석됨)               |
| **방식**         | 동기 – `require()`가 완료될 때까지 멈춤     | 비동기적 설계 – 병렬적으로 로딩 가능           |
| **특징**         | `require()`는 함수처럼 즉시 모듈 로드        | `import`는 **최상단에만** 사용 가능, 정적 분석 |

---

<br>

- **CommonJS**는 `require()`를 **코드가 실행되는 그 순간**에 모듈을 불러온다.  
  → 다음 줄로 넘어가기 전에 **모듈이 모두 로드될 때까지 기다린다.** → **동기적 방식**

- **ES Modules**는 `import`를 **코드 실행 전에 미리 분석해서** 불러올 준비를 한다.  
  → 전체 모듈 구조를 파싱하고, **비동기적으로 로딩될 수 있도록 설계**되어 있다.


</div>
</details>
