# Entry 소개 및 유형

### Webpack Entry

- webpack 으로 묶은 모든 라이브러리들을 로딩할 시작점 설정
- a,b,c 라이브러리를 모두 번들링한 bundle.js를 로딩함
- 1개 또는 2개 이상의 엔트리 포인트를 설정할 수 있음.

### 여러가지 Entry 유형

```js
const config = {
    // #1 - 간단한 entry 설정
    entry: './path/to/my/entry/file.js',
    // #2 - 앱 로직용, 외부 라이브러리 용
    entry: {
        app: './src/app.js',
        vendors:'./src/vendors.js'
    },
    // #3 - 페이지당 불러오는 js 설정
    entry: {
        pageOne:'./src/pageOne/index.js',
        pageTwo: './src/pageTwo/index.js',
        pageThree: './src/pageThree/index.js'
    }
}
```

### Multiple Entry points

- 앞에 복수개 엔트리 포인트에 대한 설정 예시

```js
// webpack.config.js
module.exports = {
    entry: {
        Profile:'./profile.js',
        Feed: './feed.js'
    },
    output: {
        path: 'build',
        filename:'[name].js'    // 위에 이정한 entry 키의 이름에 맞춰서 결과 산출
    }
};
```