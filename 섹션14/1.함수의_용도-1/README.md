섹션14 함수지향-값으로서의 함수와 콜백	
함수의 용도 - 1

자바스크립트에서는 함수도 객체다.

자바스크립트 함수가 다른 언어의 함수와 다른 점은 함수가 값이 될 수 있다는 점이다.
```
function a(){}
```
위 처럼 함수를 선언하는 데 a라는 변수에 함수가 담겨 있는 것이다.
```
var a= function(){}
```
이것과 같다.

함수는 객체의 값(value)으로도 포함이 가능하다. 

객체에 속성 값으로 담겨진 함수를 메소드라고 부른다.
```
a = { 
b:function(){
}
}	
```
키가 변수의 역할이고, 객체 안에서 변수의 역할을 하는 것을 속성(property)이라고 한다.

이 속성에 저장되어 있는 값이 함수라면 메서드라고 한다.

함수는 값이기 때문에 다른 함수의 인자로도 전달이 된다.
```
function cal(func, num){
return func(num)
}
```
func 첫번 째 인자로 담긴 함수의 인자를 두번째 인자로 받은 값을 전달해 리턴을 한다는 의미다.

```
function increase(num){
return num+1
}
```


```
function decrease(num){
return num-1
}
```

	```
alert(cal(increase, 1));
```
cal 함수의 인자값으로 increase 함수 값을 전달했다. 그리고 두번째 인자 값을 1을  준다.
그러면 
cal의 리턴 값은 increase 함수의 리턴값과 같아진다.
즉 리턴값은 2가 된다.
```
alert(cal(decrease, 1));
```

이렇게 함수가 인자값으로 들어갈 수 있다.
