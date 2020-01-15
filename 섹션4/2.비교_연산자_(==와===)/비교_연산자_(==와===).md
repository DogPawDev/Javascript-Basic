섹션4 비교
비교 연산자 (==과 ===)

동등 연산자 == 
좌항과 우항을 비교해 값이 같으면 True 다르면 False를 반환 한다. 
숫자는 비교 연산이 다른 언어들과 같지만 문자열은 약간의 차이를 보인다. 추후 알아 내야 할 듯 
alert(1==2)             //false
alert(1==1)             //true
alert("one"=="two")     //false 
alert("one"=="one")     //true
일치 연산자 === 
strict (엄격한) 동등 연산자.
좌항과 우항이 정확하게 같을 때 true 다르면 false
중요한 점은 정확하게의 의미이다.
좌항과 우항의 값이 같은 것 뿐만 아니라 데이터 타입도 같아야 true를 반환한다.
//===사용하기
alert(1=='1');              //true
alert(1==='1');             //false

기존 == 은 데이터의 값에 대해서 일치함을 중점으로 참 거짓을 판단하지만  ===은 데이터의 값과 자료형이 동일해야 참과 거짓을 판단한다.
기존 프로그래밍의 언어와 다른 점이 있다. 

== 보다 ===를 더 사용해주자.
==는 오류의 가능성이 생긴다. 
추후에 프로그램이 커지면서, 실행하는 과정에서 생기면 골치 아픔
코딩을 하는 과정에 에러를 찾는 것이 가장 이상적

alert(null == undefined); //true
alert(null === undefined); //false
alert(true == 1); //true
alert(true === 1); //false
alert(true == '1'); //true
alert(true === '1'); //false
alert(0 === -0); //true
alert(NaN === NaN); //false


