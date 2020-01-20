섹션15 함수지향 - 클로저	
private variable

```
function factory_movie(title){
return {
get_title : function (){
return title;
},
set_title : function(_title){
title = _title
}
}
}
ghost = factory_movie('Ghost in the shell');
matrix = factory_movie('Matrix');
alert(ghost.get_title());
alert(matrix.get_title());
ghost.set_title('공각기동대');
alert(ghost.get_title());
alert(matrix.get_title());
```
팩토리 무비 함수는 객체를 반환한다. 

get_title, set_title의 메서드를 담고 있는 컨테이너 = 객체를 ghost에 반환함.

여기서도 함수 호출은 이미 종료된 후에도 ghost 객체를 통해 아까 인자값으로 넣었던 ghost in th shell 이라는 문자열 변수에 접근이 가능하다.


동일한 외부함수 안에서 만들어진 내부함수들은 외부함수의 지역변수를 공유함.

그런데 똑 같은 외부함수를 공유하고 있는 ghost, matrix의 결과 값은 서로 다른데 외부함수가 실행될 때 마다 새로운 지역변수를 포함하는 클로저를 생성한다. 즉 서로 완전히 

독립된 객체가 된다.

외부함수의 지역변수인 title은 get_title을 통해서만 접근 할 수 있다. 즉 title의 수정은 해당 객체의 메서드에서만 수정이 가능하다. 

set 메소드를 통해 수정을해도 matrix 객체는 수정 안됨.

자바스크립트는 private 속성을 지원하지 않기 때문에 클로저의 이러한 특성을 이용해 구현한다.

private 속성은 객체 내부에서만 사용되는 값이 노출됨으로서 생길 수 있는 오류를 줄일 수 있다.

누구나 수정이 가능하면 유지보수에 많은 부담이된다. 이렇게 사용하면 해당 객체를 통해 접근이 가능하기 때문에 수정을 할 때 더 간편해진다.

즉 다른 사람이 title 이라는 변수의 값을 또 사용하던 어떻게 사용하던 상관이 없어진다.

set_tilte로 데이터를 수정할 때도 문자열 일때만 수정이 되도록 더 수정을 할 수도 있게끔 데이터의 수정이 어렵게 만든다.
