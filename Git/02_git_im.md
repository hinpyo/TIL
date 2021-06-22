# Git Intermediate

> Git 의 중급과정

- 모든 git repo 에는 README.md .gitignore 가 있다.
- 최초의 커밋인 root commit 은 저걸 이용해서 한다.
- VScode 편집기 설치(code로 열기 옵션 선택)
- setting `ctrl`+`(백틱) 누르기, 우측화살표에 select default profile 누른담에 git bash 선택



### commit 메세지 바꾸기

**직전 커밋만 바꿀 수 있음**

```
$ git commit --amend

# VIM 화면 등장 -> 바꿔저장
```



## .gitignore

git 이 관리하길 원치 않는 파일/폴더들을 정리한 파일

prog 이 DB 읽는데 필요한 비밀번호 등을 써놔야 할 때, API key 등등..

https://gitignore.io

https://www.toptal.com/developers/gitignore

쓰이는 언어/프레임워크 쓰고 생성 누르면 텍스트 생성됨

해당 내용 복사해서 .gitignore 파일에 붙여넣으면 됨

repo 마다 1개 (이상) 만들어줘야 함



## Local Branching

브랜치를 따게(만들게)되면 현재 brach의 모든 상황을 복사하여 평행세계(?)를 만든다.

새롭게 로그인 기능을 구현한다던지 할 때 기능단위로 사용함.

새로운 branch 가 성공적으로 작동한다면 그제서야 master를 옮겨준다. (병합-merge)

branch 를 줄기라 생각하면 개념이해가 어렵고 최종 commit을 가리키는 pointer 라고 이해하는 것이 좋음.

- 시초의 branch가 master

- 여태까진 master branch에 커밋을 한거임, 그 중에서 줄기가 master가 아니라 줄기의 가장 최신/마지막 commit이 master 이다.
- HEAD 란 지금 내가 있는 곳 or 내가 보고있는 곳 (내 눈이 있는 곳), 터미널에서 파란 괄호로 나오는 게 HEAD가 현재 가리키는 곳임 eg. (master), (aaa)
- git log 찍으면 나오는 엄청 긴 문자가 고유값임, 이것을 알아야 HEAD를 옮길 수 있음(과거로 돌아가는 등)

```
$ git checkout <oneline 에서 나오는 4글자정도>

# 복귀하기
$ git checkout master
```



### create branch

```
# 브랜치 생성 (마지막 commit을 새로운 브랜치 name으로 가리킴)
$ git branch <new-branch-name>

# 브랜치 목록 확인
$ git branch

# 브랜치 이동
$ git switch <branch-name>

# 브랜치 병합(merge)
$ git switch master
$ git merge <branch-name>
```

```
# 브랜치 생성 후 이동 (한 번에)
$ git switch -c <new-branch-name>  #-c는 create 옵션
```



### delete branch

```
# merge 완료된 브랜치 삭제
$ git branch -d <branch-name>

# merge 미완료된 브랜치 강제 삭제
$ git branch -D <branch-name>
```



### merge(두개의 brach를 병합)

1. Fast Forwarding (꽃길)

   혼자 브랜치 사용하여 작업하면 대부분 이렇게 됨

   ```
   (master)
   $ git branch aaa
   
   (master)
   $ git switch aaa
   
   (aaa)
   $ 
   
   # ... 수정 수정 ....
   
   (aaa)
   $ git add .
   $ git commit -m 'aaa1'
   $ git switch master
   
   (master)
   $ git merge aaa
   $ git branch -d aaa  #역할을 다 했으므로 삭제
   ```

2. Conflict - Auto merge (충돌 & 자동 병합)

   branch commit 한 상태에서 master도 commit 하면 충돌 발생

   이 경우에 merge 하면 새로운 commit(Merge branch) 생성되며 병합됨

   자동으로 merge 되는건 순전히 운이 좋아서임(수정한 부분--변경점-- 중에 겹치는 부분이 없기 때문)

   ```
   # 그림으로 보기
   $ git log --oneline --graph
   ```
   1. a 브랜치에서 커밋
   2. mater 브랜치에서 커밋
   3. (master)  $ git merge a
   4. **운이 좋아** 두 커밋이 겹치지 않음
   5. 자동으로 merge 완료

   ```
   # 명령어 병합하기
   $ git add . && git commit -m 'message'
   ```

   

3. Conflict - Manual merge (충돌 & 수동 병합)
   1. a 브랜치에서 커밋
   2. mater 브랜치에서 커밋
   3. (master)  $ git merge a
   4. 두 커밋이 겹치는 구간이 있음
   5. 수동으로 충돌 해결 후 저장
   6. `git add` , `git commit`



요즘은 핵심 branch 이름을 master 가 아닌 main 으로 밀고있음



## Remote Branching











## 협업 Collaborating

1. 조장이 remote 생성

   1. `README.md`, `.gitignore'`생성하며 리포 만들기
   2. settings > manage access 에서 팀원 추가

2. 모든 팀원이 remote repo 를 local 에 clone

3. branch 생성 후 각자 개발 진행

4. 완료 후 해당 branch 의 내용을 remote 로 push (origin 에 feature/pay 를 push)

5. 코드 작성자가 remote 에서 PullRequest(MergeRequest) -> 결제요청을 진행

6. 팀 합의에 따라 변경내용을 master로 `merge`

   1. 충돌(conflict)이 난다면, 논의 후 `Resolve confilcts` 로 리모트에서 직접 수정
   2. `commit merge` 로 확정

   - (commit만 이동하고 branch는 안 넘어옴)

7. 팀원들은 local master 에서 `git pull origin master` 를 통해 모든 변경 내용을 pull
8. 3번으로











