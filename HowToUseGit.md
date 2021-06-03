# How to use Git

### 1. 윈도우의 경우 git 설치 (맥은 생략 가능)

Cmd 에서 git --version 으로 설치 유뮤 확인 가능



### 2. Github 가입

가입하고 레포지토리 만들기



### 3. Github에 올리고 싶은 디렉토리로 들어가기

#### 이동시 유용한 쉘 명령어

방향키 위로 누르면 이전 명령어 뜸

파일명이 directory_name_is_too_long 일 경우 dire 정도만 쓰고 tab 누르면 자동완성 해줌

`pwd`  현재 내가 있는 위치 확인하는 명령어

`ls` 현 디렉토리에 있는 디렉토리, 파일등 확인

`cd ..`  상위 폴더로 이동

`cd temp`  temp  디렉토리로 이동(temp 자리에 원하는 디레토리 명 기입)

`mkdir temp` temp 디렉토리 생성

`touch temp` temp 파일 생성

`rm 파일이름` 파일 삭제

`rm -r 디렉토리 이름` 디렉토리 삭제 



vi 에디터 에서 나오고자 할때 ESC :q! 

작성한 내용을 저장하고 종료시 ESC :wq



### 4. Git 최초 설정하기

`git init` .git 폴더 생성(깃 레포지토리 ls -a 로 확인 가능)

`git config --global user.name "본인이름"`

`git config --global user.email "본인 이메일"`

`git add .` 현 디렉토리의 변경사항 모두 스테이지에 올림 . 대신 파일명 작성시 그 파일만 올라감

`git status` 현 상황 확인 가능

* untracked 깃이 관리하지 않는 파일 (add 명령어로 관리하는 파일로 변경 가능)
* unmodified 변경사항 없음
* modified 변경사항 있음
  * 빨간색으로 뜰 경우 add가 안 되어 있는 상태

`git commit -m "업데이트 사항 작성"`

`git remote add origin 레포지토리 주소` 원격 저장소 주소 등록

`git push origin master` 변경사항 원격 저장소에 게시 

로그인 완료하면 push 완료 됨



`git pull origin master` 업데이트 된 사항 내려받기 

`git clone 레포지토리 주소` Github 에서 소스를 받을 때 



### 5. 취소하기

되돌리는 것은 지양하는 것이 좋음

`git reset add를 취소하고자 하는 파일명` 파일명 생략시 모두 취소 됨

`git reset HEAD^` 커밋 취소하고 파일 unstated 상태로 돌아감

`git reset --hard HEAD` 마지막 커밋 상태로 되돌림