섹션9 객체(object)

객체와 반복문
```
var grades = {'egoing': 10, 'k8805': 6, 'sorialgi': 80};
for(key in grades) {
    document.write("key : "+key+" value : "+grades[key]+"<br />");
}
```

배열은 저장된 데이터들이 순서를 가지고 있다.

먼저 들어온 것과 나중에 들어온 것들이 기록이 되어 있다.

즉 배열에 추가된 것 자체로 중요한 정보다.

하지만 객체는 주어진 순서는 없고 키와 밸류가 쌍으로 저장 되어있다.

그렇기 때문에 반복문으로 객체를 접근하게 되면 순서대로 나오지 않는다.

객체를 하나하나 꺼내오기 위해선 새로운 반복문을 사용해야한다.

key 라는 변수에 grades 객체 안에 있는 키를 반복문이 실행 될 때마다 한 개씩 가져온다.
  ```
  var grade = {'test':1,'test2':2,'test3':3};
            for(key in grade){
                document.write(`<li>Key : ${key} value : ${grade[key]} \n</li>`)
            }
 ```
위의 자바스크립트 코드가
 

 ![p1](/img/s9_5_2.PNG)

html 문서에서 다음과 같이 나타나는데 이렇게 자바 스크립트 언어로 html을 제어 할 수 있다.

이게 자바스크립트가 나온 이유였다

백틱이라는 것을 활용하면 문자열을 사용할 때 보다 간단하게 사용 할 수 있다.

자바스크립트를 이용해 프로그래밍 적으로 웹페이지를 생성 한 것



참고로 for in 문법은 배열에서도 사용이 가능하다.
```
for(var name in arr){
 console.log(name);
console.log(arr[name]) // 인덱스 접근	
}
```





