섹션12 자바스크립트와 정규표현식
치환

본문 URL 을 링크 html 태그로 교체하는 코드
```
var urlPattern = /\b(?:https?):\/\/[a-z0-9-+&@#\/%?=~_|!:,.;]*/gim;
var content = '생활코딩 : http://opentutorials.org/course/1 입니다. 네이버 : http://naver.com 입니다. ';
var result = content.replace(urlPattern, function(url){
    return '<a href="'+url+'">'+url+'</a>';
});
console.log(result);

```
정규표현식을 저렇게 쓰는 이유는 더 공부를 해서 알아봐야 한다.

본문 내용에서 URL을 찾아 링크를 걸어주는 코드다.
```
content.replace(urlPattern, function(url){
url 부분은 처음 가저오는 url 패턴이 들어간다 즉 http://opentutorials.org/course/1 이 부분이 들어간다.
});
```
