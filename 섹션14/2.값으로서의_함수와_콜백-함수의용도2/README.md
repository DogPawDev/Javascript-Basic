섹션14 함수지향-값으로서의 함수와 콜백	
값으로서의 함수와 콜백- 함수의 용도 2




리턴값으로의 함수의 사용
```
function cal(mode){
    var funcs = {
        'plus' : function(left, right){return left + right},
        'minus' : function(left, right){return left - right}
    }
    return funcs[mode];
//cal의 인자값이 plus가 들어오고 반환 값이 funcs객체를 반환하면서 거기안에 있는 메서드에 접근이 가능해 진다. 그러면서 ‘plus’의 함수가 실행이 된다
}
alert(cal('plus')(2,1));
//그렇기 때문에 함수의 인자값인 (2,1)이 들어가는 것이다.
alert(cal('minus')(2,1));
```
배열으로서의 함수의 사용
```
var process = [
    function(input){ return input + 10;},
    function(input){ return input * input;},
    function(input){ return input / 2;}
];
var input = 1;
for(var i = 0; i < process.length; i++){
    input = process[i](input);
}
alert(input);
```
함수가 변수, 매개변수, 리턴값으로도 활용이 가능하다.
first-class citizen,object 라고 불리운다.
