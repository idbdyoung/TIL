# tsconfig.json 살펴보기

## 1. compilerOptions

> 컴파일 옵션을 설정하는 속성. 생략가능하며 생략하면 기본값이 사용된다.

> **-- target**
>
> > 타입스크립트 파일을 컴파일 했을 때, 빌드 디렉토리에 생성되는 자바스크립트의 버전
>
> - "ES3" (기본 값)
> - "ES5"
> - "ES6"/"ES2015"
> - "ES2016"
> - "ES2017"
> - "ES2018"
> - "ES2019"
> - "ES2020"
> - "ESNext" (최신 ES 제안 기능을 대상)

> **-- lib**
>
> > 컴파일에 포함될 라이브러리 파일 목록
>
> > 지정되지 않으면 target 옵션에 지정된 버전의 기본 리스트가 삽입.

> **-- module**
>
> > 자바스크립트 파일간 import 문법을 구현할 때 어떤 문법을 쓸지 정함
>
> - AMD
> - commonjs (require) (IE 호환)
> - ESNEXT (import)

> **-- allowS**
>
> > JavaScript 파일의 컴파일을 허용

> **-- skipLibCheck**
>
> > 활성화 되면(true)일 경우 선언 파일(d.ts)에서 발생하는 모든 오류 무시
>
> > 라이브러리 코드에서 오류가 발생하거나 컴파일 시간이 너무 오래 걸리는 경우 활성화

> **-- esModuleInterop**
>
> > Commonjs방식으로 내보낸 모듈을 es모듈 방식의 import로 가져올 수 있게 해줌

> **-- strict**
>
> > 모든 엄격한 타입 검사 옵션을 활성화

> **-- forceConsistentCasingInFileNames**
>
> > 파일명에 대소문자 구분하지 않아도 되는 기능 사용 여부
>
> > true: 대소문자 반드시 구분
> > false: 대소문자 구분하지 않음

> **-- moduleResolution**
>
> > 모듈을 해석하는 방식
> >
> > - `Classic` 방식
> > - `Node` 방식
> > - https://typescript-kr.github.io/pages/module-resolution.html (참고)
>
> > 모듈(module)방식이 "AMD" 또는 "SYSTEM" 또는 "ES6"라면 Classic 방식
>
> > 그 외는 Node

> **-- jsx**
>
> > JSX 코드를 어떻게 컴파일할지 결정 (tsx 확장자에만 영향을 준다)
>
> - `react` : js 파일로 컴파일 된다. (JSX 코드는 React.createElement() 함수의 호출로 변환됨)
> - `preserve` : jsx 파일로 컴파일 된다. (JSX 코드가 그대로 유지됨)

> **-- outDir**
>
> > 컴파일 후 생성되는 js파일이 생성될 폴더명
>
> - 프로젝트를 js 에서 ts로 마이그레이션 하게 되면 allowJS 옵션을 true로 해주어야 하는데 이때 ouDir를 반드시 지정해 주어야 tsconfig 파일이 에러가 나지 않는다.

## 2. include , exclude

> - include : 컴파일할 파일 경로를 설정
>
> - exclude: 컴파일 제외 파일 경로 설정
>
> ex)
>
> ```
>   {
>    "include": [
>        "src/**/*.ts" //src 디렉터리 안의 모든 .ts 확장자 컴파일
>    ],
>    "exclude": [
>        "node_modules"
>    ],
>   .
>   .
> ```
