섹션19 객체지향-생성자와 new	
생성자와 new
생성자는 객체를 만드는 역할을 하는 함수다.

자바스크립트 함수는 단순하게 재사용 가능한 로직의 묶음이 아니라 객체를 만드는 창조자다.

```
function person(){}
var p0 = ();
```
p0 아무것도 없다
하지만

var p = new Person()

이렇게 선언하면

객체가 생성된다.

new 앞에 함수는 생성자라고 부른다.

객체의 생성자

var p = {} 와 동일하게 볼 수 있다.

함수가 객체의 창조자다.

자바스크립트에서 생성자는 자바처럼 클래스가 없기 때문에 함수 가 객체가 된다.
```
ex 1)
function Person(){}
var p = new Person();
p.name = 'egoing';
p.introduce = function(){
    return 'My name is '+this.name; 
}
document.write(p.introduce());
ex2)
function Person(){}
var p1 = new Person();
p1.name = 'egoing';
p1.introduce = function(){
    return 'My name is '+this.name; 
}
document.write(p1.introduce()+"<br />");
 
var p2 = new Person();
p2.name = 'leezche';
p2.introduce = function(){
    return 'My name is '+this.name; 
}
document.write(p2.introduce());


ex 3)
function Person(name){
    this.name = name;
    this.introduce = function(){
        return 'My name is '+this.name; 
    }   
}
var p1 = new Person('egoing');
document.write(p1.introduce()+"<br />");
 
var p2 = new Person('leezche');
document.write(p2.introduce());
```
생성자내에서 객체의 속성을 정의하고 있다 -> 초기화 -> 재사용성이 높아진다.
