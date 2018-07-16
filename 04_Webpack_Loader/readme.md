# Loader 소개

#### Webpack Loader

- 웹팩은 자바스크립트 파일만 처리가 가능하도록 되어 있다.
- loader 를 이용하여 다른 형태의 웹 자원들을 (img, css, ...) js로 변환하여 로딩

```js
module.exports = {
    entry: {
        // ...
    },
    output: {
        // ...
    },
    module: {
        rules: [
            { test: /\.css$/, use: ['style-loader','css-loader'] }
        ]
    }
};
```

- loader 에서 모듈 로딩 순서는 배열의 요소 오른쪽에서 왼쪽으로 진행됨.

```
{
    test: /backbone/,
    use: [
        'expose-loader?Backbone',
        'imports-loader?_=underscore,jquery'
        // 순서대로 (1) juqery, (2) underscore 로딩
    ]
}
```

https://github.com/webpack-contrib/expose-loader

https://github.com/webpack-contrib/imports-loader

https://webpack.js.org/concepts/loaders/

# Babel Loader

- preset : Babel 플러그인 리스트

```js
module: {
    rules: [{
        test: /\.js$/,
        use: [{
            loader:'babel-loader',
            options: {
                presets: [
                    ['es2015', 'react', {modules:false}]
                ]
            }
        }]
    }]
}
```

```
//.babelrc 
{
    "presets":["react","es2015"]
}
```