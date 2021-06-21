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









