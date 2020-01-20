섹션15 함수지향 - 클로저	


내부함수, 외부함수

내부함수

자바스크립트는 함수 안에서 또 다른 함수를 선언할 수 있다. 아래의 예제를 보자. 결과는 경고창에 coding everybody가 출력될 것이다.
```
function outter(){
function inner(){
var title = 'coding everybody'; 
alert(title);
}
inner();
}
outter();
```
위의 예제에서 함수 outter의 내부에는 함수 inner가 정의 되어 있다. 함수 inner를 내부 함수라고 한다.

내부함수는 외부함수의 지역변수에 접근할 수 있다. 아래의 예제를 보자. 결과는 coding everybody이다.

어떤 함수가 있는데 그 함수에서만 사용하는 함수가 있다면 이렇게 내부함수를 만들어 주는게 좋다

다른 곳에선 쓰이지 않는데 함수 밖에 정의를 내리면 응집성이 떨어지므로 보기 좋지 않다.



```
function outter(){
var title = 'coding everybody'; 
function inner(){ 
alert(title);
}
inner();
}
outter();
```
위의 예제는 내부함수 inner에서 title을 호출(4행)했을 때 외부함수인 outter의 지역변수에 접근할 수 있음을 보여준다.

외부함수에 정의되어 있는 타이틀 지역변수가 내부함수에서 호출되고 있다.

내부 함수에서 title이라는 변수가 없으면 밖에서 해당 변수를 찾는다

내부함수에서 외부함수의 지역변수에 접근 할 수 있다. 이를 클로저라고 한다.
