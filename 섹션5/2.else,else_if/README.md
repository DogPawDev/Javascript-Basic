섹션5 조건문
else,else if
if 만으로는 복잡한 상황을 처리하기에 부족하기 때문에 if 가 거짓이라면 실행하는 부분이 있어야 한다.

example) if else
//ex 1)

if(true){
    alert(1);
} else {
    alert(2);
}

//ex 2)

if(false){
    alert(1);
} else {
    alert(2);
}
example) else if
//ex 1)
if(false){
    alert(1);
} else if(true){
    alert(2);
} else if(true){
    alert(3);
} else {
    alert(4);
}
// 결과 : 2

//ex 2)
if(false){
    alert(1);
} else if(false){
    alert(2);
} else if(true){
    alert(3);
} else {
    alert(4);
}
//결과 3

//ex 3
if(false){
    alert(1);
} else if(false){
    alert(2);
} else if(false){
    alert(3);
} else {
    alert(4);
}

