# Git의 역사
분산 버전 관리 시스템(DVCS)
Bitkeeper가 유료화 상용해서 리누스 토발즈가 Git을 직접 만듦.(GPL(공개라이센스)를 따라야함.)
# Github 이야기
Github는 개발자들의 놀이터
Github는 Mit라이센스방식인데 공개된 소스코드를 무료로 사용하고 업그레이드할경우 공개할 의무는 없다라는 방식.
# 분산관리 시스템
VCS - 버전관리 시스템 
전체 복사를 하지않고 부분변경을해서 시간과 용량을 잡아먹지 않는다.
단점) 바이러스에 취약, 협엽이 안됨

CVCS(SVN) - 중앙 집중형 버전관리 시스템(협업)
단점) 업데이트 이슈로 협업을 잘해야함, 중앙 시스템에 의존

DVCS(Git) - 분산버전관리 시스템
# Git 3가지 영역
git init - 깃을 시작하겠어

작업 영역(폴더) - 변경 감지

git add - 변경이 된 파일만 가져옴

인덱스 영역(트리)(해시코드로 관리) - 변경된 파일이 BLOB개체로됨 

git commit - 영구적으로 기록함

헤더 영역(브랜치) - 버젼으로 영구적 기록

버전마다 복구가 가능하고 트리별로 지우더라도 인덱스 영역 전체가 백업이 되어있이서 복구가능

# Git 기본기 실습
형상관리(SCM) - 변경사항을 체계적으로 추적,통제하는 것

git init - 깃을 시작하겠어

![image](https://github.com/se6in/Git-study/assets/116144890/c9f473fa-0017-44e7-959a-9f95257dcd14)

숨김 폴더가 생김

![image](https://github.com/se6in/Git-study/assets/116144890/51084826-0d36-4618-b73d-13b7720bdcc2)

git status - 현재 작업(Working tree)의 상태를 찍어볼 수 있는 명령어이다. 

변경사항(Changes)이 있는지 없는지 여부와 staging이 되었는지 commit할 것이 있는지 등을 알려준다.

![image](https://github.com/se6in/Git-study/assets/116144890/4bd74777-c5e3-4895-bc8c-a0f6c170061b)

test1.txt파일이라는 변경사항이 있으니 인덱스 영역에 기록하고 싶다면 git add로 가져와라.

git add . - 변경된 모든 파일 add

git add test1.txt - test1.txt 파일 add 

![image](https://github.com/se6in/Git-study/assets/116144890/b7450d06-8049-4b30-82bc-5f14bba59832)

.git(숨김폴더) > objects > 새로운폴더 > 새로운 해시값 파일 생성된다.

![image](https://github.com/se6in/Git-study/assets/116144890/8619d860-401e-45fc-bc86-7e0c08fd4151)

git commit을 최초로하면 설정이 안되어있어서 안된다.

이렇게 기초설정을 해준다.

![image](https://github.com/se6in/Git-study/assets/116144890/72273352-81f8-4e26-a102-d66f71b4ec92)

git config --list - git 기초설정의 리스트를 볼 수 있다.

git log -  헤더 영역에 영구히 저장된 로그를 볼 수 있다.

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

git commit ammend -m "" - 가장 최근의 커밋을 수정함 

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

