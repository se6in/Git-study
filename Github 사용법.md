# Github push(업로드+병합)

github 클라우드 저장소를 origin이라고한다. 연결을해줘야한다.

![image](https://github.com/user-attachments/assets/479c63ba-9efa-4357-81c7-ece5c5c0892c)


git remote add origin 주소를 하면 연결됨

git remote -v - 연결상태를 나타냄

git ls-remote - 연결상태를 나타냄

git push orgin master(마스터브랜치) - 파일업로드,병합을 해주는 명령어

업로드됨

![image](https://github.com/user-attachments/assets/cefc99cb-0fd0-416c-87f3-c2bb8fddc46e)

# Github pull(다운로드+병합)

git remote rm origin - 리모트 삭제하는것

git pull origin master - 다운로드하는것

![image](https://github.com/user-attachments/assets/f3428f7f-8a73-43a4-9e5a-822311d7fb5c)

# Github clone

git clone 깃허브주소 - git init(시작),git remote(연결),git pull(다운) 한번에 해줌.

(마스터 브랜치만 동기화 나머지 브랜치는 체크아웃해서 생성 및 병합해줘야함.)

![image](https://github.com/user-attachments/assets/f9f25d02-ec69-40e0-bfdc-f5555752781f)

# Github 초보자 체험

(상황1)

회사에서 작업을 완료하면 push로 파일을 완료하고 집에서 더 작업하고 싶으면 pull로 파일을 다운받아 동기화 시켜준다.

새로운 작업환경에서 작업하면 clone을 쓴다.

(상황2)

다른환경에서 작업을 하다가 멈췄을때는 브랜치를 바꿔서 push 한다.

![image](https://github.com/user-attachments/assets/04455f86-5fd8-4004-b427-015c0242b193)

회사로 돌아오고나서 데이터 동기화를 위해 pull을 해준다.

그리고 topic 브랜치를 다운받아야한다.

git fetch origin - 모든 패치를 다운받는다.

git checkout -b topic origin/topic - 브랜치 생성 및 머지

![image](https://github.com/user-attachments/assets/cacd9288-5150-4313-a0c8-e03313ba9c6f)

# Github remote branch

1. git clone으로 마스터브랜치를 가져온다.

2. git check out -b dev origin/master

3. git check out -b topic origin/master
