섹션5 조건문
논리 연산자

AND 연산자 &&  곱하기를 생각하면 된다.
좌항과 우항 중 하나라도 0(거짓)이면 거짓이고 모두다 참일 때 참이다.

OR 연산자 ||  더하기와 같다. 
좌항과 우항 중 하나라도 1(참)이면 참이고 모두가 거짓일 때 거짓을 반환 한다.

! 부정 연산자
Boolean의 값을 역전 시킨다.

ex 1) &&
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8"/>
</head>
<body>
    <script>
        id = prompt('아이디를 입력해주세요.');
        password = prompt('비밀번호를 입력해주세요.');
        if(id=='egoing' && password=='111111'){
            alert('인증 했습니다.');
        } else {
            alert('인증에 실패 했습니다.');
        }
    </script>
</body>
</html>
ex 2) || 를 이용한 예제 개선
id = prompt('아이디를 입력해주세요.');
password = prompt('비밀번호를 입력해주세요.');
if((id==='egoing' || id==='k8805' || id==='sorialgi') && password==='111111'){
    alert('인증 했습니다.');
} else {
    alert('인증에 실패 했습니다.');
}

