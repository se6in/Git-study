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
