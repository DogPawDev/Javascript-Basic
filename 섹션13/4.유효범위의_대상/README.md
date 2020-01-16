섹션13 함수지향-유효범위	
유효범위의 대상

다른 언어들과 다르게 자바스크립트는 함수에 대한 유효범위만을 제공한다.
```
for(var i = 0; i < 1; i++){
var name = 'coding everybody';
}
alert(name);
```
함수에서 선언한 것이 아니기 때문에 name은 전역변수 취급이다.

자바
```
for(int i = 0; i < 10; i++){
String name = "egoing";
}
System.out.println(name);
//에러
```
