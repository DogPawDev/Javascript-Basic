섹션9 객체(object)
객체 지향 
```
var grades = {
    'list': {'egoing': 10, 'k8805': 6, 'sorialgi': 80},
    'show' : function(){
        for(var name in this.list){
            document.write(name+':'+this.list[name]+"<br />");
        }
    }
};
grades.show();
```

객체안에 객체를 다시 넣을 수 있다.
만약 리스트안에 egoing을 접근하려면
```
grades[‘list’][‘egoing’]) 이렇게 하면 10이 출력된다.
```
함수도 담을 수 있다.

선언된 함수를 호출하려면 grades[‘show’]());

함수도 값으로 생각하기 때문에 즉 변수에 저장 할 수 있어서 객체에 함수가 들어가는 것이다.

this는 약속되어 있는 변수다.

this는 현재 자신이 속해있는 위치에 객체를 가르킨다. 말 그대로 자기 자신이 속해있는 객체를 가르킴

grades 객체 변수 안에 데이터 (list)와 행위 (show)가 함께 저장 되어 있는데 이렇게 사용하는 방식을 객체 지향 이라고 한다.


