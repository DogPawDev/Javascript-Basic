섹션10 모듈
모듈화
모듈이 없다면?
```
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8"/>
</head>
<body>
<script>
function welcome(){
return 'Hello world'
}
alert(welcome());
</script>
</body>
</html>
```

만약 welcome 이라는 함수가 다른 몇 백개의 페이지에서도 사용을 한다면 수정이 이루어 질 경우 모두다 수정해야함


```
<head>
<script src=”greeting.js”> < /script>
</head>
```
이렇게 외부파일을 읽어와 자바스크립트를 사용 할 수 있다.

해당 파일만 수정하면 된다.
