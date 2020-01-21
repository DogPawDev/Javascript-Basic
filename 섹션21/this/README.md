
섹션21 객체지향-this
this  = 이것


this는 함수 호출 맥락을 의미

맥락에 따라서 파악한다. -> 어떤 의미가 고정되어 있지 않고 사용하는 것에 따라 의미가 달라진다.

함수와 객체의 관계가 느슨한 JS에서 둘을 연결시켜주는 연결점 역할을 한다.

this는 함수 안에서 사용하는 일종의 변수 이면서 약속 되어있는 값, aruments 처럼 

함수호출

함수를 호출 했을 때 this는 

window 와 같다.

함수가 어느 객체에 소속되어 있지 않으면 window 전역객체를 가리킨다.

그냥 함수를 호출할 때 window 객체의 메소드이기 때문에 this를 하면 window를 가리키는 것

메소드와 this

메소드가 속해있는 객체에 this로 접근 할 수 있다. 

객체에 속해있는 함수 = 메소드일 경우 속해있는 객체를 가리킨다.

생성자와 this
```
ex)
var funcThis = null; 
 
function Func(){
    funcThis = this;
}
var o1 = Func();
if(funcThis === window){
    document.write('window <br />');
}
 
var o2 = new Func();
if(funcThis === o2){
    document.write('o2 <br />');
}
```


객체로서 함수
```
var sum2 = new Funcion(‘x’,’y’,’return x+y;’);
```
이렇게 작성하면 
```
function sum(x,y){return x+y;}
```
이 내용과 같다.

함수를 쉽게 작성할 수 있도록 문법을 지원해주는 것이다.

함수 리터럴 이라고 한다.

Literal


o = {}
new object
객체 리터럴 이라고 부른다 
a=[1,2,3] 

배열 리터럴
new array(1,2,3)
값을 만들어주는 문법적인 체제 = 리터럴

apply와 this

스위치 문
같은 타입의 케이스에 실행이 된다.
```
var o = {}
var p = {}
function func(){
    switch(this){
        case o:
            document.write('o<br />');
            break;
        case p:
            document.write('p<br />');
            break;
        case window:
            document.write('window<br />');
            break;          
    }
}
func();
func.apply(o);
func.apply(p);
apply(o) func가 O의 메소드로 들어가기 때문에 this의 객체는 o가 된다.
```
객체 – 주인
메소드 – 노예
