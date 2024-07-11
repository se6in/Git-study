# [Git의 기초](https://github.com/se6in/Git-study/blob/main/Git%EC%9D%98%20%EA%B8%B0%EC%B4%88.md)
# [Git의 기본기실습](https://github.com/se6in/Git-study/blob/main/Git%20%EA%B8%B0%EB%B3%B8%EA%B8%B0%20%EC%8B%A4%EC%8A%B5.md)


# Git 중급(섹션2)

![image](https://github.com/se6in/Git-study/assets/116144890/95fb9e2d-c0c9-4128-995f-05b6c8eda24e)

잘못 커밋했을때는 git reset 명령어를 쓴다

git reset soft - 커밋로그 변경시

![image](https://github.com/se6in/Git-study/assets/116144890/e48ed380-0893-4af6-9c88-a6a4c77fde8e)

헤더 상태가 커밋전으로되고 git add . 만 된 상태로 바뀜.

git reset mixed - 작업 영역의 내용 변경시 필요(잘안씀)

git reset hard - test1 상태로 돌아가길 원해(test2 파일까지 지워져서 잘 써야함.)

git reflog - 한번이라도 커밋한것이 남아있음.

![image](https://github.com/se6in/Git-study/assets/116144890/75e01061-f742-4c6b-b85a-1ebec7da31ad)

git commit --amend -m "" - 가장 최근의 커밋을 수정함 

# Git 고급(섹션3)

Branch란 여러 개발자들이 동시에 다양한 작업을 할 수 있게 만들어 주는 기능

![image](https://github.com/se6in/Git-study/assets/116144890/6e9b689a-ae4d-4d3a-a2a4-891bf0610a79)

메인 브랜치가 있고 필요한 기능별이나 개선사항이 있을때마다 브랜치를 생성한다.

fast-foward merge 방법

topic 브랜치에서 아이디 중복체크 완료를 커밋하면 topic브랜치포인터는 아이디 중복 체크 완료를 가르키고

fast-foward merge하면 메인 브랜치포인터도 아이디 중복 체크완료를 가르킨다.

![image](https://github.com/se6in/Git-study/assets/116144890/adaeb228-8e54-40d7-b685-1f8c1dde68c2)

3-way merge 방법

topic 브랜치에서 아이디 중복체크 완료를 커밋하고 topic브랜치포인터는 아이디 중복 체크 완료를 가르키고

메인 브랜치에서 글쓰기를 커밋하면 가지가쳐진다. 이때 fast-foward merge하면 글쓰기 파일이 날라간다.

로그인,아이디 중복완료, 글쓰기를 3-way merge한다.

![image](https://github.com/se6in/Git-study/assets/116144890/d15a872c-3df4-460a-8530-dc5b5675f62e)

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
