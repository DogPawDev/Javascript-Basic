섹션12 자바스크립트와 정규표현식
옵션(I,g)

정규표현식에는 옵션이라는 것이 있다. 

정규 표현식이 동작하는 방식을 다르게 만들어 줄 수 있다.

옵션은 여러 개가 있으며 그중 i와 g에 대해서 알아본다.	

i는 대소문자를 구분하지 않도록 한다.
```
var xi = /a/;
console.log("Abcde".match(xi)); // null
var oi = /a/i;
console.log("Abcde".match(oi)); // ["A"];
```

g는 검색된 모든 결과를 리턴 한다.

이 옵션을 사용하지 않으면 가장 첫 번째 a를 만나면 바로 종료 한다. 

하지만 g 옵션을 넣어주면 문자열에 포함되어 있는 모든 a를 배열에 담아서 리턴을 해준다.

```
var xg = /a/;
console.log("abcdea".match(xg));
var og = /a/g;
console.log("abcdea".match(og));
```

위 두개를 합쳐 사용이 가능하다
var ig = /a/ig;
