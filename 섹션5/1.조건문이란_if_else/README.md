섹션5 조건문
조건문이란? (if, else)

Conditional Steatement
주어진 조건에 따라 실행을 다르게 동작하도록 하는 것

조건이 될 수 있는 값은 무조건 Boolean 이다. 
참이라면 다음 중괄호 구문이 실행이 된다.
참이 아니라면 {} 중괄호 내용은 무시하고 진행 된다.

example) if
```
//ex 1)
if(true){
    alert('result : true');
}

//ex 2)
if(false){
    alert('result : true');
}

//ex 3)
if(true){
    alert(1);
    alert(2);
    alert(3);
    alert(4);
}
alert(5);

//ex 4)
if(false){
    alert(1);
    alert(2);
    alert(3);
    alert(4);
}
alert(5);
 ```
중간에 alert이 여러 번 호출 되는 상황이 오는데 자바스크립트 번역기가 사용자가 경고창을 닫을 때 까지 기다렸다가 다음 구문을 실행 한다.

![p1](/img/s5_1_1.png)