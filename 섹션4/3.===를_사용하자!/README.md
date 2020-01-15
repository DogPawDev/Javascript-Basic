
섹션4 비교
===를 사용하자!
```
alert(null === undefined); //false
alert(true == 1); //true
alert(true === 1); //false
alert(true == '1'); //true
alert(true === '1'); //false
alert(0 === -0); //true
alert(NaN === NaN); //false
alert(null == undefined); //true
```

null 은 값이 없다라는 의미. 
undefined는 값이 정의되질 않았다는 의미. 
비슷해 보이지만 정확하게 따지면 다르다.
null은 값이 없지만 변수를 통해 프로그래머가 의도해서 null을 지정했다.
undefined는 프로그래머와 의도가 없다. 
== 연산자로 바라보면 데이터의 값이 없다는 측면에서는 같다고 확인 할 수 있지만
=== 연산자로 바라보면 값이 없는 것과 아예 정의가 안돼 있는 것은 다르다고 판단한다.

자바스크립트는 	
```
boolean
number
string
undefined
null
``` 
이런 자료형이 있다.
== 연산자는 true 를 1과 동일하게 본다. false는 1이 아닌 모든 것들을 다 거짓으로 판단 한다.
number, string 둘다 1 , ‘1’ 을 참으로 확인함.
=== 연산자는

NaN === NaN
0/0 과 같이 성립하지 않은 것은 NaN 타입으로 나오는데 이는 계산할 수 없는 것들을 말한다.
이 둘을 === 비교하면 무조건 거짓으로 나타낸다.

![p1](/img/s4_3_1.png)

![p1](/img/s4_3_2.png)

다음과 같이 비교 했을 때 나타나는 값을 그래프로 확인 할 수 있다.
비교하는 연산자를 사용할 땐 왠만하면 ===를 사용하자.
