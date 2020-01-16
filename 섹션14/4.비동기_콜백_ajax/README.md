섹션14 함수지향-값으로서의 함수와 콜백	
비동기 콜백과 ajax	

서비스 운영 측면에서 비동기 콜백이 없으면 한 서비스가 실행 될 때마다 계속 기다려야한다 .
Ajax를 활용한다
Asynchronous Javascript and XML
자바스크립트를 통해 서버와 통신해서 가져와라 
```
datasource.json.js
{"title":"JavaScript","author":"egoing"}
```
demo1.html
```
<!DOCTYPE html>
<html>
<head>
<script src="//code.jquery.com/jquery-1.11.0.min.js"></script>
</head>
<body>
<script type="text/javascript">
    $.get('./datasource.json.js', function(result){
        console.log(result);
    }, 'json');
</script>
</body>
</html>

```