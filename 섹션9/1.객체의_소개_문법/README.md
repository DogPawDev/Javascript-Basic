섹션9 객체(object)

객체의 소개와 문법

배열과 비슷한 점을 가졌다.

배열은 연관된 데이터를 담아내기 위한 그릇이였다면 

객체 역시 연관된 데이터를 담아내기 위함이 있다. 하지만 배열은 인덱스 번호를 이용해 접근을 했다면 번호가 아닌 이름을 부여해 이름으로 접근을 할 수 있다. 직접 프로그래머가 

지정해서 만들 수 있다는 점이 가장 큰 차이점이다.

객체는 키와 밸류가 묶여서 사용된다.

객체를 만드는 법은 여러가지가 있다.
```
var grades = {'egoing': 10, 'k8805': 6, 'sorialgi': 80};

var grades = {};
grades['egoing'] = 10;
grades['k8805'] = 6;
grades['sorialgi'] = 80;

var grades = new Object();
grades['egoing'] = 10;
grades['k8805'] = 6;
grades['sorialgi'] = 80;
```

접근하는 방법
```
var grades = {'egoing': 10, 'k8805': 6, 'sorialgi': 80};
alert(grades['sorialgi']);
```
키는 문자이기 때문에 만약 [ ‘egoin’+’g’] 이렇게 해도 접근이 가능하다.
```
alert(grades.sorialgi);
```
하지만 . 을 사용해 접근을 할 때는 문자열로 인식하지 않는다. 대괄호를 사용할 때 문자열로 인식이 가능
는 방법
