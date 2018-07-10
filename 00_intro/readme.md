## 수업 소개

webpack - module bundler

## 수업 개요

- React, Vue에서 권고하는 Webpack 설정에 대해 학습 및 이해
- Webpack의 주요 설정 Entry, Output, Loader, Plugins, Resolve 학습 및 실습
- 실무에 적용할 수 있는 Webpack 개발환경 설정방법 학습 및 실습


## webpack 이란?

- 서로 연관 관계가 있는 웹 자원들을 js, css, img 와 같은 스태틱한 자원으로 변환해주는 모듈 번들러

- 모듈 관리가 수월함, 성능을 끌어올림

## Webpack 을 사용하는 이유 & 배경

1. 새로운 형태의 Web Task Manager ( 기존 Web Task Manager (Gulp, Grunt)의 기능 + 모듈 의존성 관리 )
2. 자바스크립트 Code based Modules 관리

## 자바스크립트 모듈화 문제란?

```html
<script src="module1.js"></scrpt>
<script src="module2.js"></scrpt>
<script src="module3.js"></scrpt>
```
- 전역변수 충돌, 스크립트 로딩 순서, 복잡도에 따른 관리상의 문제
- 이를 해결하기 위해 webpack이 등장

