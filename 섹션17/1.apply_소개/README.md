섹션17 함수지향 – 함수의 호출	
apply 소개

자바스크립트는 특별한 함수 호출 방법을 지원한다.

함수라는 것도 객체이다.

객체는 속성들을 가지고 있다.

그 속성의 값이 저장이 되어 있다면 속성이라고 부르고

그 속성이 함수면 메소드라고 부른다.

함수라는 객체에는 메소드라는 객체를 가지고 있다.

```
function func(){
}
func();

func.call
func.apply

```
이렇게 두개의 미리 정의된 메소드를 사용할 수 있다.

둘다 함수 호출을 하는 메소드이다.

내장된 코드일 경우 native code 라고 보여진다.


```
function sum(arg1, arg2){
return arg1+arg2;
}
alert(sum.apply(null, [1,2]))
```
위 코드에서 sum(1,2)와 sum.aplly(null,[1,2]) 실행 결과가 같다.
apply 두번째 인자 값에 배열을 넣어주면 정의한 매개변수에 들어간다.

첫번째 인자는 null 이 들어가면 그냥 함수 호출이랑 동일한 것 이렇게 쓰면 안된다.
