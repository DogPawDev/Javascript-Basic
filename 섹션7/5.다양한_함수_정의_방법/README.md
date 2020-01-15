섹션7 함수

다양한 함수 정의 방법
```
var numbering = function (){
    i = 0;
    while(i < 10){
        document.write(i);
        i += 1;
    }   
}
numbering();
```

기존 함수 정의 방식과 다른데

변수가 함수를 가지게 되는 것이다.



익명 함수 

1회성으로 호출 할 때 사용하는 방식이다.

```
(function (){
	i=0;
	while(i<10){
		document.write(i);
		i+=1;
}
})();

```


