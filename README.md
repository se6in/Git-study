# [Git의 배경지식(섹션0)(역사,이야기,분산관리시스템)](https://github.com/se6in/Git-study/blob/main/Git%EC%9D%98%20%EA%B8%B0%EC%B4%88.md)
# [Git 초급(Git 3가지 영역, 기본기 실습)](https://github.com/se6in/Git-study/blob/main/Git%20%EA%B8%B0%EB%B3%B8%EA%B8%B0%20%EC%8B%A4%EC%8A%B5.md)
# [Git 중급(reset,reflog,amend)](https://github.com/se6in/Git-study/blob/main/Git%20%EC%A4%91%EA%B8%89.md)

# [Git 고급(branch,fast-forward merge,3-way merge 이해)](https://github.com/se6in/Git-study/blob/main/Git%20%EA%B3%A0%EA%B8%89.md)

## fast-foward merge 실습

git touch 파일명.확장자 - 현재 위치에서 새로운 파일 생성

git branch - 현재 브랜치 확인

![image](https://github.com/se6in/Git-study/assets/116144890/57cd7fd7-89b6-4979-a285-801d1fd76373)

git branch 이름 - 새로운 브랜치 생성

![image](https://github.com/se6in/Git-study/assets/116144890/021e7b60-39d4-434f-b759-ba589263dd62)

마스터 브랜치포인터, 토픽 브랜치포인터 둘다 로그인을 가르킴

![image](https://github.com/se6in/Git-study/assets/116144890/1cd7deda-bdaf-4afd-a556-f4575e563dd1)

git checkout 이름 - 이름 브랜치로 이동

![image](https://github.com/se6in/Git-study/assets/116144890/8a4b2859-287d-427c-be7f-a0ab08081f7d)

topic 브랜치로 이동 후 아이디중복체크를 생성하고 add하고 커밋하고 로그를보면 마스터 브랜치포인터는 로그인에, 토픽 브랜치포인터는 아이디중복체크에 간걸 알 수 있음.

![image](https://github.com/se6in/Git-study/assets/116144890/f35c8485-992b-41cb-8109-dc16666d3d30)

마스터브랜치에서 git merge topic을 하면 토픽브랜치를 마스터브랜치에 합치겠다는 뜻

![image](https://github.com/se6in/Git-study/assets/116144890/5ad712aa-fb09-4b6b-8f5c-51d10caedbfe)

## 3-way merge 실습

git checkout -b 이름 - 이름 브랜치를 생성하면서 브랜치 이동 

![image](https://github.com/se6in/Git-study/assets/116144890/d6ff4a7c-a635-4b08-98dc-328e25e0b233)

현재 토픽브랜치에서 아이디 중복체크 파일을 만들고 커밋하고 메인 브랜치에서 글쓰기 파일을 만들고 커밋한상태이다.

병합할려고 git merge topic한다.

![image](https://github.com/se6in/Git-study/assets/116144890/d5c38710-42b3-4498-922b-edcf5dad36e2)

vi에디터가 나오는데 esc후 :wq 하면 저장 후 3-way merge가 된다.

![image](https://github.com/se6in/Git-study/assets/116144890/10576e38-a340-4f0a-bbf3-4e68ad546a6f)

로그 찍어보면 병합이 되었다.

![image](https://github.com/se6in/Git-study/assets/116144890/174f09b0-3519-42ea-9f5a-4d5a81955ac5)

# Git merge 충돌

(현재상황)

마스터 브랜치와 토픽브랜치가 같은 파일을 수정해서 커밋하고 병합할 때 내용일 달라서 충돌이 일어난다.

![image](https://github.com/se6in/Git-study/assets/116144890/18ca1e79-c0b7-4ffe-8155-2e0b8a72852d)

![image](https://github.com/se6in/Git-study/assets/116144890/9db0cc27-a3b9-4844-b0f8-c717c8e38eab)

웬만하면 브랜치를 나누면 같은 파일을 수정하지않는다.

# Git rebase 로그 관리

rebase - 로그 정리를 깔끔하게한다.

(현재상황)
로그인 커밋을 하나로 만들고 싶음.

![image](https://github.com/se6in/Git-study/assets/116144890/23bdff96-0c3e-4d8b-8f7c-df42ef29267b)

VI에디터 들어와서 i키를 누르면 인서트가된다

![image](https://github.com/se6in/Git-study/assets/116144890/3ae1310e-2534-43c5-a3bb-8f6d2e72ca4a)

스쿼시(찌그러뜨리다)할 부분을 s로 바꿔준다.

esc하고 :wq해준다.

![image](https://github.com/se6in/Git-study/assets/116144890/135bcf51-acd0-4239-b771-599ef780d83d)

로그인 완료만 남기고 싶으니깐 로그인 퇴근 , 로그인 꾀병부려서퇴근을 지운다.

(#은 모두 주석이라 신경 ㄴㄴ)

esc하고 :wq해준다.

![image](https://github.com/se6in/Git-study/assets/116144890/7b784a10-ffc9-4e5e-a399-b4bda59d743f)

![image](https://github.com/se6in/Git-study/assets/116144890/1e918eb3-e320-40ae-af47-6a5575b1c73a)
