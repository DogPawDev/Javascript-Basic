섹션17 함수지향 – 함수의 호출	
apply 사용
```
ex 1)
o1 = {val1:1, val2:2, val3:3}
o2 = {v1:10, v2:50, v3:100, v4:25}
function sum(){
    var _sum = 0;
    for(name in this){
        _sum += this[name];
    }
    return _sum;
}
alert(sum.apply(o1)) // 6
alert(sum.apply(o2)) // 185
```

sum() 함수에서 this는 호출 될 때 정해진다.

sum.apply(o1) 이렇게 객체를 넣어서 호출을 하게 되면

함수 내부에서 this[name] 부분이 객체가 들어가게 된다.

즉 객체 안에 속성들을 다 더한 값이 반환 된다.

즉 sum 함수안에 var this= o1; 이 추가된 것이다.

this가 o1의 객체를 가리키고 있다. 즉 for in 문을 사용해 this에서 name 변수에 객체의 키들을 한 개씩 꺼내온다.

apply를 사용하게 되면 

o1.sum 이렇게 실행이 되는 것이다.

즉 sum이 o1 객체에 메소드로 들어가는 것

o1 = {val1; ~~~~ sum:sum}

typeof this[name] !== ‘funcion’)
