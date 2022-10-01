# 48장 모듈

## 48.1 모듈의 일반적 의미

- 애플리케이션을 구성하는 개별적 요소로서 재사용 가능한 코드 조각
- 자신만의 파일 스코프(모듈 스코프를 가짐)
- 캡슐화되어 다른 모듈에서 접근 불가
  - 모듈의 자산은 비공개(변수, 함수, 객체 등)
  - 애플리케이션과 분리되어 존재
- 공개가 필요한 자산에 한정하여 명시적으로 선택적 공개가 가능(exprot라 함)
- 모듈이 공개(export)한 일부 또는 전체를 자신의 스코프 내로 불러들여 재사용 가능(import라 함)

## 48.2 자바크스킯트와 모듈

- 자바스크립트의 태생적 한계로 인해 모듈 시스템을 지원하지 않음
- script 태그를 사용하여 외부의 자바스크립트 파일을 로드할 수 있지만 파일마다 독립적인 스코프를 갖지 않는다. 하나의 전역 스코프를 공유한대.
- 서버 사이드에서 자바스크립트를 사용하려는 움직임이 생기면서 극복해야하는 핵심과제가 됨
  - 제안된 것이 CommonJS, AMD
  - Node.js에서는 CommonJS를 채택
  - Node.js에서는 파일별로 독립적인 파일 스코프를 갖는다.

## 48.3 ES6 모듈(ESM)

- ES6에서는 클라이언트 사이드에서도 동작하는 모듈 스코프 기능을 추가
- IE를 제외한 브라우저에서 사용 가능
- script 태그에 type="module" 어트리뷰트를 추가하여 동작

### 48.3.1 모듈 스코프

예제 파일 참고

### 48.3.2 export 키워드

- 모듈은 독자적은 모듈 스코프를 갖음
- 당연히 모듈 내부 선언한 식별자는 내부에서만 참조 가능
- 외부에서 사용하려면 export 키워드

예제 참조 
- lib.mjs

### 48.3.3 import 키워드

- 다른 모듈에서 export한 식별자를 자신의 모듈 스코프 내부로 로드하려면 import 키워드 사용

예제 파일 참고
- app.mjs