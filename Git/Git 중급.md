# Git 중급

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
