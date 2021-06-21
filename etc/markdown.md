# MD 배우기

개발자의 문서양식 markdown 을 배웁니다.



## 제목

'#'의 개수에 따라 제목의 중요도가 달라집니다.

'#' 1개는 h1임. h는 heading의 약자로 h1~6까지 있음.

h1=> 문서에서 가장 큰 제목, 문서에서 1개만 사용 가능

문서에 h1과 h3만 있으면 잘못 작성된 문서



## 본문

본문은 그냥 적으면 본문이에요



## 리스트

### 순서 있는 리스트(1.)

1. 식용유를 두른다.
2. 파를 넣고 파기름을 낸다.
3. 계란을 풀어서 익힌다.
4. 간장을 볶는다.

### 순서 없는 리스트(-)

- '-' 친담에 띄어쓰기
  - tab을 눌러서 들여쓰기
    - 한번 더 들여쓰기
  - shift tab은 내어쓰기
- cli, git, md 학습
- cli에서 tab 쓰기



## 인라인 코드(``)

파일을 생성하기 위해서 `touch` 명령어를 사용한다.

`cd`를 통해 폴더간 이동을 한다.



## 코드블럭(```언어)

```
$ touch a.txt
$ rm a.txt
$ mkdir test
$ cd test
```

```python
def my_func(num):
	num += 1
	return num
	
print(my_func(1))
```

```javascript
function myfunc(num) {
    return num++
}

console.log(myfunc())
```



## 표(|a|b|c|)

* cli 단축키

| 단축키       | 설명        | 사용예시                  |
| ------------ | ----------- | ------------------------- |
| `ctrl`+`c`   | 취소        | 뭔가 안될 때 누르기       |
| `ctrl + l`   | 비우기      | 기존 화면을 위로 밀기     |
| `ctrl` + `w` | 단어 지우기 | 한 글자씩 지우면 힘들어요 |

행 추가는 ctrl enter

*(애스터리스크)

|(파이프)



## 수식($$)

$$
\begin{align*}
y = y(x,t) &= A e^{i\theta} \\
&= A (\cos \theta + i \sin \theta) \\
&= A (\cos(kx - \omega t) + i \sin(kx - \omega t)) \\
&= A\cos(kx - \omega t) + i A\sin(kx - \omega t)  \\
&= A\cos \Big(\frac{2\pi}{\lambda}x - \frac{2\pi v}{\lambda} t \Big) + i A\sin \Big(\frac{2\pi}{\lambda}x - \frac{2\pi v}{\lambda} t \Big)  \\
&= A\cos \frac{2\pi}{\lambda} (x - v t) + i A\sin \frac{2\pi}{\lambda} (x - v t)
\end{align*}
$$

typora latex(타이포라 레이텍) 검색해서 써보기

* 많이 쓰이는 양식임, 디스코드에서도 ` 같은거 먹는다



## 볼드처리(**)

이것은 **굵어**질거야



## TIL 프로젝트

today i learned 

오늘 내가 배운것들

1일 1커밋 힘들다, but 공부한거 남기려면 이거 남기면 됨



## 수평선(---)



## 이미지

캡쳐따는법 프린트 스크린 누르고 붙여넣기 ㄴㄴ

`window` + `shift` + `s` 한담에 붙여넣기

markdown.assets 폴더 안에 이미지 파일이 들어감

![](markdown.assets/image-20210621144709669.png)



## Git

* home~ root/
* cd 만치면 홈으로
* 폴더에서 우클릭 후 git bash
* home 이 아닌 폴더에서!! git init 하면 .git 폴더생성과 함께 추가기능 생기며 업글됨, 이 폴더를 리포 or 저장소라 부름
* (master)는 리포의 상징
* rm -rf .git 하면 되돌리는 거 가능

* ls -a all의 약자 -r 는 리커시브, -f 는 force 강제로

- 유닉스에서 .으로 시작하는 파일/폴더는 숨겨진거



* git status
* git add  <FILENAME>
* git commit -m 'Commit Message' (m은 메세지의 약자)
* git config --global user.email ""
* git config --global user.name "" (configuration 설정)
* 확인은 ""만 빼고 쳐보면 됨
* git log
* 깃은 변경사항만 저장(용량의 낭비를 막기 위해서)
* 커밋 = 스냅샷 = 사진 ??
* 무조건 add 후에 commit 해야함



| Working Dir   | Staging Area | Repository |
| ------------- | ------------ | ---------- |
| 분장실        | 스테이지     | 사진       |
| 코드를 수정함 | add->        | commit->   |



