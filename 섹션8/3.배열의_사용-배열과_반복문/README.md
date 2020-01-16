섹션8 배열

배열의 사용 – 배열과 반복문

배열의 진가는 반복문과 결합하면 나타난다.

배열의 크기가 커지면 인덱스 값을 전부다 기억 할 수 없기 때문에 배열을 하나하나 가져와서 사용하는 것이 좋다. -> 반복문과 연결이 된다.
```
function get_members(){
    return ['egoing', 'k8805', 'sorialgi'];
}
members = get_members();
// members.length는 배열에 담긴 값의 숫자를 알려준다. 
for(i = 0; i < members.length; i++){
    // members[i].toUpperCase()는 members[i]에 담긴 문자를 대문자로 변환해준다.
    document.write(members[i].toUpperCase());   
    document.write('<br />');
}
 ```
