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

git status - 현재 작업(Working tree)의 상태를 찍어볼 수 있는 명령어이다. 변경사항(Changes)이 있는지 없는지 여부와 staging이 되었는지 commit할 것이 있는지 등을 알려준다.

![image](https://github.com/se6in/Git-study/assets/116144890/4bd74777-c5e3-4895-bc8c-a0f6c170061b)
test1.txt파일이라는 변경사항이 있으니 인덱스 영역에 기록하고 싶다면 git add로 가져와라.

git add . - 변경된 모든 파일 add

git add test1.txt - test1.txt 파일 add 

![image](https://github.com/se6in/Git-study/assets/116144890/b7450d06-8049-4b30-82bc-5f14bba59832)

.git(숨김폴더) > objects > 새로운폴더
![image](https://github.com/se6in/Git-study/assets/116144890/8619d860-401e-45fc-bc86-7e0c08fd4151)
