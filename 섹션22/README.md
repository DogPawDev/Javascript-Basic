섹션22 객체지향-상속

1.	상속이란?

객체지향에서 중요한 요소

객체는 하나의 컨테이너이고 변수와, 메소드를 가지고 있다.

이런 객체의 특성을 그대로 물려 받아 새로운 객체를 만들 수 있다.


부모 객체 자식 객체 이렇게 만들 수 있는데 상속받은 객체에서 원본 객체에 변수와 메서드를 사용할 수 있다.

그뿐만 아니라 변수를 추가하거나 메소드를 보완하거나 추가 할 수 있다. -> 재활용이 가능하다.
```
function Person(name){
this.name = name;
this.introduce = function(){
return 'My name is '+this.name; 
} 
}
var p1 = new Person('egoing');
document.write(p1.introduce()+"<br />");
```

함수안에서 할당
```
function Person(name){
this.name = name;
}
Person.prototype.name=null;
Person.prototype.introduce = function(){
return 'My name is '+this.name; 
}
var p1 = new Person('egoing');
document.write(p1.introduce()+"<br />");
```
밖에서 할당

위코드는 같다.

상속을 위한 기본적인 준비 

2.	상속의 사용법
```
function Person(name){
    this.name = name;
}
Person.prototype.name=null;
Person.prototype.introduce = function(){
    return 'My name is '+this.name; 
}
 
function Programmer(name){
    this.name = name;
}
Programmer.prototype = new Person();
 
var p1 = new Programmer('egoing');
document.write(p1.introduce()+"<br />");
```

프로그래머도 사람 

프로그래머에 메서드를 정의하지 않아도 사용이 가능

3.	기능의 추가
물려받는 것만이 아니라 추가, 수정도 가능하다.
```
function Person(name){
    this.name = name;
}
Person.prototype.name=null;
Person.prototype.introduce = function(){
    return 'My name is '+this.name; 
}
 
function Programmer(name){
    this.name = name;
}
Programmer.prototype = new Person();
Programmer.prototype.coding = function(){
    return "hello world";
}
 
var p1 = new Programmer('egoing');
document.write(p1.introduce()+"<br />");
document.write(p1.coding()+"<br />");
```
프로토타입이 중요하다.

4.	prototype
```
function Ultra(){}
Ultra.prototype.ultraProp = true;
 
function Super(){}
Super.prototype = new Ultra();
 
function Sub(){}
Sub.prototype = new Super();
 
var o = new Sub();
console.log(o.ultraProp);
```
접근하는 것이 없다면 부모의 부모의 부모 를 찾아가 찾아낸다.

함수는 생성자이기도 한데 new 명령어를 만나 생성자 함수를 객체로 만들어 리턴을 한다.

객체는 {} 이렇게 만들어줘도 되지만 초기값을 정해주고 객체를 만들어주고 싶기 때문에 new sub()이렇게 사용

각 함수에는 prototype 이라는 객체를 저장할 수 있는 프로퍼티가 있다.

5.	prototype chain

```
function Ultra(){}
Ultra.prototype.ultraProp = true;
 
function Super(){}
Super.prototype = new Ultra();
 
function Sub(){}
Sub.prototype = new Super();
 
var o = new Sub();
console.log(o.ultraProp);

```

1.	객체 o에서 ultraProp를 찾는다.
2.	없다면 Sub.prototype.ultraProp를 찾는다.
3.	없다면 Super.prototype.ultraProp를 찾는다.
4.	없다면 Ultra.prototype.ultraProp를 찾는다.

o에 ultraProp 가 없으면 o의 생성자를 찾아 해당 변수를 찾는다.

주의 할 점 

상속을 할 때
```
var a = new Super();
sub.prototype = a 이렇게 상속은 해도 되지만
sub.protoype = Super.prototype 을 넣어주면 안된다
```
new를 사용해야한다. 

저렇게 할 경우 sub 객체에 무언가 추가하면 부모 객체에도 추가가된다.
