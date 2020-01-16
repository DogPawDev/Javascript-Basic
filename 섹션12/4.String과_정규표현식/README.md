섹션12 자바스크립트와 정규표현식
String과 정규표현식
```
var pattern = /a/;
var str = ‘abcdef’l
```
문자열 객체의 메서드인 match에 인자값을 정규표현식 패턴을 넣어주면 해당 문자가 있으면 해당 문자를 배열의 원소로 반환한다. 없으면 null 반환

str.match(pattern);

치환

str.replace(pattern,’A’);

정규표현식의 패턴을 찾아 ‘A’로 치환 함

‘Abcdef’
