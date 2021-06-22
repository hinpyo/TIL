# Git basic

git 의 기초를 배워봅시다



## WARNING

1. Home 폴더(~)를 리포로 업그레이드 하지 않는다.(git init)
2. 리포 안에 리포를 만들지 않는다 (리포의 하위 폴더에서 다시 'git init' 하지 않는다.



## 저장소 초기화 하기

```
$ git init
```



## 저장소를 일반 디렉토리로 되돌리기

```
rm -rf .git
```



## Stage 에 올리기(Staging)

특정 파일만 스테이지에

```
$ git add <FILENAME>
```

현재 위치의 모든 파일을 (알아서 변경사항 있는 파일만)

```
$ git add .
```



## Stage 에서 내리기(unstage)

```
$ git restore --staged <FILENAME>
```



## 복구하기(이전 버전으로)

```
$ git restore <FILENAME>
```



## commit 을 통해 스냅샷 저장하기

```
$ git commit (-m) "MESSAGE"
```

-m은 message 옵션

안쓰려면 'git add . 내용 추가'



## 잘못올린 commit 취소하기

```
$ git reset HEAD~
```

head 를 한 칸 뒤로(변경사항은 그대로 두고)

```
$ git reset --hard HEAD~
```

변경사항까지 되돌리기

* GitHub 에서 공동작업시 reset 하면 꼬이기 쉬우니 주의



## 현재 상태 확인하기

```
$ git status
```

- 빨간색으로 표시되는 파일은 commit에 포함되지 않음
- 초록색으로 표시되는 파일은 commit에 포함됨
- 변경사항이 없는 파일은 표시되지 않음



## 커밋 로그 확인하기

```
$ git log (--oneline)
```

- 로그 너무 길어서 프로그램으로 넘어가면 q로 빠져나오기

- oneline 옵션은 1줄만 출력하는거



## vim

i, `esc`, :w (write), :q(quit), :q!(강제종료)

i : 편집모드

esc: 명령모드

: : ??모드



## 숙제

1. 개발용 메일 준비
2. 개발용 메일로 git config --global user.email ""
3. 이 메일로 깃헙 가입
   1. username에 대문자/공백 섞지않기
   2. username이 개발자 닉네임





## Git Repository

local 과 remote로 구분

1:N 구성이 가능(local repo : N remote repo)

대표적 remote repo 플랫폼 github, bitbucket, gitlab

1. github 에 repo 만들기
2. local 과 연결하기

```
$ git remote add origin https://github.com/hinpyo/TIL.git
$ git remote -v

$ git remote --help
$ git remote remove <NAME>
$ git remote rename <old> <new>
```

- remote add 까지는 고정, origin 은 URL의 별칭(편하게 쓰기 위한, origin이 default 값), 뒤에는 URL
- 주소 복사하고 `insert`누르면 편하게 
- remote -v 로 확인하는듯
- help 눌러서 가능한 명령어 확인
- remove 로 삭제, rename으로 이름 수정

3. 업로드(push)

```
$ git push origin master
```

- git이 origin(별칭)으로 업로드(push)를 한다
- git bash에 파란색 괄호에 master 혹은 main 이라 돼 있는걸로 따라서

편집점 발생









