섹션5 조건문
Boolean의 대체제
조건문에서 꼭 True와 False 만 사용할 수 있는 것은 아니다.
1 (참)
0 (거짓)
하지만 이렇게 쓰지 말기 

빈 문자열 FALSE
undefined FALSE
값이 할당되지 않은 변수 null FALSE 
NaN FALSE
조건문에 사용될 수 있는 데이터 형이 꼭 불린만 되는 것은 아니다. 관습적인 이유로 0는 false 0이 아닌 값은 true로 간주된다. 아래의 예제는 2를 출력한다.
```
if(0){
    alert(1)
}
if(1){
    alert(2)
}
```
기타 false로 간주되는 데이터 형
다음은 false와 0 외에 false로 간주되는 데이터형의 리스트다. if문의 조건으로 !(부정) 연산자를 사용했기 때문에 각 조건문의 첫번째 블록이 실행되는 것은 주어진 값이 false이기 때문이다.
```
if(!''){
    alert('빈 문자열')
}
if(!undefined){
    alert('undefined');
}
var a;
if(!a){
    alert('값이 할당되지 않은 변수'); 
}
if(!null){
    alert('null');
}
if(!NaN){
    alert('NaN');
}

```

다음 표를 참고하자

![p1](/img/s5_5_1.png)

참고 https://dorey.github.io/JavaScript-Equality-Table/