# NPM 소개

- js 라이브러리들을 모아놓은 열린 공간
- font-end web apps, mobile app, robots, routers 라이브러리들이 존재
- Gulp, Webpack 모두 node 기반, NPM 을 사용하여 필요 라이브러리들이 존재
- 재사용이 가능한 code 를 module, package 라고 호칭
- package.json : 해당 package 에 대한 파일 정보가 들어가 있음.
- keyword 로 패키지 검색 가능 

# NPM 명령어

### Package.json 생성

- 프로젝트의 node module 들 관리를 위한 package.json 설정
- -y 를 붙이면 default 정보를 가지고 package.json 을 설정

```
npm init
npm init -y
```

### 패키지 설치 및 업데이트

- 프로젝트에서 사용할 node module 설치 및 package.json 업데이트

```
npm install 패키지명 --save
npm i 패키지명 --save
```

### Global 설치 vs Local 설치

```
npm i gulp -global
npm i gulp
```

global은 시스템레벨에서 설치되고 local은 해당 프로젝트의 node_modules에 들어가게됨.

### install --save vs --save-dev

- --save 는 앱이 구동하기 위해 필요한 모듈 & 라이브러리 설치. ex) react, vue

```
//  package.json
"dependencies": {
    "vue":"^2.3.3"
    ...
},
```

- --save -dev 는 앱 개발시에 필요한 모듈 & 라이브러리 설치. ex) test, build tool, live reloading

```
//  package.json
"devDependencies": {
    "gulp":"^3.9.1",
    ...
}
```