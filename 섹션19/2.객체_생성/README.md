섹션19 객체지향-생성자와 new	
객체 생성
var person = {} ; 비어 있는 객체 

비어 있는 객체에 담는 방법

person.name = ‘egoing’;

person 객체 안에 name이라는 변수에 egoing을 담았다.
객체안에 변수를 속성 – 프로퍼티라고 부른다.

함수는 메서드이다. (방법)

this는 객체를 가르킨다.

위 방식은 객체를 만드는 과정이 분리되어 있어서 혼란을 줄 수 있다.





객체란 서로 연관된 변수와 함수를 그룹핑한 그릇이라고 할 수 있다. 객체 내의 변수를 프로퍼티(property) 함수를 메소드(method)라고 부른다. 객체를 만들어보자.
```
var person = {}
person.name = 'egoing';
person.introduce = function(){
    return 'My name is '+this.name;
}
document.write(person.introduce());
```
객체를 만드는 과정에 분산되어 있다. 객체를 정의 할 때 값을 셋팅하도록 코드를 바꿔보자.
```
var person = {
    'name' : 'egoing',
    'introduce' : function(){
        return 'My name is '+this.name;
    }
}
document.write(person.introduce());
``
만약 다른 사람의 이름을 담을 객체가 필요하다면 객체의 정의를 반복해야 할 것이다. 객체의 구조를 재활용할 수 있는 방법이 필요하다. 이 때 사용하는 것이 생성자다.


이렇게 만들어서 이대로 사용을 한다면
name 다를 수 있지만 메서드는 동일하게 작동을 하는 상황에서 메서드를 수정하게 되면 전부 수정을 해줘야하는 일이 벌어진다.

생성자, new 통해 해결이 가능하다.
