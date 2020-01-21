섹션23 객체지향- 표준 내장객체의 확장






1.	배열의 확장 1,2
```
ex)
var arr = new Array('seoul','new york','ladarkh','pusan', 'Tsukuba');
function getRandomValueFromArray(haystack){
    var index = Math.floor(haystack.length*Math.random());
    return haystack[index]; 
}
console.log(getRandomValueFromArray(arr));
 ```
random 함수는 소수점을 반환하기 때문에 정수로 만들어줘야 한다.

이상태로는 Array 객체에서 사용자가 만든 함수를 포함시키지 않는다.
	
Array 객체에 prototype에 접근해 메서드를 추가해주자.
```
ex)
Array.prototype.rand = function(){
    var index = Math.floor(this.length*Math.random());
    return this[index];
}
var arr = new Array('seoul','new york','ladarkh','pusan', 'Tsukuba');
console.log(arr.rand());
 ```
배열객체의 원형에 prototype에 함수를 추가했다.
전에는 함수에 배열을 전달해줬어야 했지만 
이미 배열 객체안에서 사용되기 때문에 this를 해주면 arr 객체를 의미하게 된다.
그래서 인자를 안 받는다.

이렇게 기본 내장 객체를 사용해 API를 확장할 수 있다.
