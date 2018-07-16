# Webpack Output

- entry 에서 설정하고 묶은 파일의 결과값을 설정

```
const path = require('path');
module.exports = {
    entry: {
        // ...
    },
    output: {
        path: path.resolve(__dirname,'dist'),
        filename:'bundle.js'
        // filename: '[name],js'
    }
}
```

## Output Name 옵션

```
output: {
   filename:'[name].js',    // 1
   filename:'[hash].js',    // 2
   filename:'[chunkhash].js'    // 3 
}
```

1. name : 엔트리 명에 따른 output 파일명 생성
2. hash : 특정 webpack build에 따른 output 파일명 생성
3. chunkhash : 특정 webpack chunk에 따른 output 파일명 생성

## 참고 API

*path.join()*

- 해당 API가 동작되는 OS의 파일 구분자를 이용하여 파일 위치를 조합한다.

```
path.join('/foo','bar','baz/asdf');
// Returns: '/foo/bar/baz/asdf'
```

*path.resolve()*

- join()의 경우 그냥 문자열만 합치지만, resolve 은 오른쪽에서 왼쪽으로 파일 위치를 구성해가며 유요한 위치를 찾는다.
- 만약 결과 값이 유요하지 않으면 현재 디렉토리가 사용된다. 반환되는 위치 값은 항상 absolute URL 이다.

```
path.resolve('/foo/bar','./baz');
// Returns: '/foo/bar/baz'

path.resolve('/foo/bar','/tmp/file/');
// Returns: '/tmp/file'

path.resolve('wwwroot','static_files/png/','../gif/image.gif');
// if the current working directory is /home/myself/node,
// this returns '/home/myself/node/wwwroot/static_files/gif/image.gif'
```