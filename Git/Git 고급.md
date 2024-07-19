# Git 고급

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
