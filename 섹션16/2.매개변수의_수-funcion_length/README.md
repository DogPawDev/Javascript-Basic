섹션16 함수지향 - arguments	

매개변수의 수 – function length
```
function zero(){
    console.log(
        'zero.length', zero.length,
        'arguments', arguments.length
    );
}
function one(arg1){
    console.log(
        'one.length', one.length,
        'arguments', arguments.length
    );
}
function two(arg1, arg2){
    console.log(
        'two.length', two.length,
        'arguments', arguments.length
    );
}
zero(); // zero.length 0 arguments 0 
one('val1', 'val2');  // one.length 1 arguments 2 
two('val1');  // two.length 2 arguments 1
```

함수에 length 를 사용해 함수가 정의한 매개변수의 수를 확인 할 수 있다. arguments 랑 비슷하면서 다른데 argument는 함수가 호출 될 때 인자값을 바라본다.
