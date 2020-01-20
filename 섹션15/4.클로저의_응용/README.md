섹션15 함수지향 - 클로저	
클로저의 응용
```
var arr = []
for(var i = 0; i < 5; i++){
    arr[i] = function(){
        return i;
    }
}
// 이렇게 반복문을 실행 할 경우 외부함수 
for(var index in arr) {
    console.log(arr[index]());
}
var arr = []
for(var i = 0; i < 5; i++){ㄱ
    arr[i] = function(id) {
        return function(){
            return id;
        }
    }(i);
}
for(var index in arr) {
    console.log(arr[index]());
}

/* 결과
0
1
2
3
4
*/
```

추후 다시 복습이 필요함
