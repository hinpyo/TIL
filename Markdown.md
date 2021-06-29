# 소개(Introduction)

- 이 문서는 공부한 것을 정리하기 위해 작성 되었으며 틀린 내용이 있을 수 있습니다.
- 이 문서는 공식 영어/한글 명칭의 사용을 지향합니다. 그 분류와 구성은 임의로 편집하였습니다.
- 이 문서는 지속적으로 update 될 예정입니다.
- 목차에 링크를 클릭하면 해당 내용으로 이동이 가능합니다. (링크 넣기 힘들어요.. 나중에 목차 생성기 만들어봐야지)
- 이 문서에서 <>로 묶인 태그는 HTML 문법이지 Markdown 문법이 아닙니다. 이외에도 표준이 아닌 내용을 해당 표준으로 분류했을 가능성이 있으니 유의 바랍니다.
- Markdown 표준이 지원하는 내용은 아주 적기 때문에 Github Flavored Markdown, MultiMarkdown 등 여러 변형판이 존재합니다. 따라서 표준을 벗어난 문법은 플랫폼 마다 지원하지 않을 수 있습니다.
- Editor로 Typora를 사용하기 때문에 단축키에 대한 정보를 추가하였습니다.  

  

## 목차(Index)

- [마크다운 문법(Markdown Syntax)](#마크다운-문법markdown-syntax)
  - [1.문단 제목(Headers)](#1-문단-제목headers)
  - [2.수평선(Horizontal Rules)](#2-수평선horizontal-rules)
  - [3.본문](#3-본문)
    - [1.강제 개행(Line Breaking)](#1-강제-개행line-breaking)
    - [2.강조(Emphasis)](#2-강조emphasis)
    - [3.인라인 코드(Inline code)](#3-인라인-코드inline-code)
    - [4.목록(Lists)](#4-목록lists)
    - [5인용문(Blockquotes)](#5-인용문blockquotes)
  - [4.첨부](#4-첨부)
    - [1.이미지(Images)](#1-이미지images)
    - [2.링크(Links)](#2-링크links)



- [GitHub Flavored Markdown Syntax](#github-flavored-markdown-syntax)
  - [1.문단 제목(Headers)](#1-문단-제목headers)
  - [2.수평선(Horizontal Rules)](#2-수평선horizontal-rules)
  - [3.본문](#3-본문)
    - [1.강조(Emphasis)](#1-강조emphasis)
    - [2.문법 강조(Syntax highlighting)](#2-문법-강조syntax-highlighting)
    - [3.순서 없는 목록(Unordered Lists)](#3-순서-없는-목록unordered-lists)
    - [4.할 일 목록(Task Lists)](#4-할-일-목록task-lists)
    - [5.마크다운 서식 무시](#5-마크다운-서식-무시)
  - [4.etc.](#4-etc)
    - [.](#)
    - [.](#)
    - [.](#)
    - [.](#)



- [Typora Shortcut](#typora-shortcut)
  - [1.제목 서식](#1-제목-서식)
  - [2.기타 서식](#2-기타-서식)
  - [3.편집](#3-편집)
  - [4.보기](#4-보기)



# 마크다운 문법(Markdown Syntax)



## 1. 문단 제목(Headers)

```
# 제목 h1 태그
## 제목 h2 태그
### 제목 h3 태그
#### 제목 h4 태그
##### 제목 h5 태그
###### 제목 h6 태그
```

# 제목 h1 태그

## 제목 h2 태그

### 제목 h3 태그

#### 제목 h4 태그

##### 제목 h5 태그

###### 제목 h6 태그



## 2. 수평선(Horizontal Rules)

```
* * *
***
*****
- - -
-----
_ _ _
```

* * *
***
*****
- - -
-----

_ _ _



## 3. 본문

### 1. 강제 개행(Line Breaking)

```
끝에 공백 두 칸  
끝에 역슬래시 넣기\
끝에 br 넣기<br>
줄바꿈 확인용 문장
```

끝에 공백 두 칸  
끝에 역슬래시 넣기\
끝에 br 넣기<br>
줄바꿈 확인용 문장



### 2. 강조(Emphasis)

```
*이탤릭체 혹은 기울임꼴*
_이탤릭체 혹은 기울임꼴_

**볼드체 혹은 굵게**
__볼드체 혹은 굵게__

_이모 **쓰까**주세요_
```

*이탤릭체 혹은 기울임꼴*
_이탤릭체 혹은 기울임꼴_

**볼드체 혹은 굵게**
__볼드체 혹은 굵게__

_이모 **쓰까**주세요_



### 3. 인라인 코드(Inline code)

```
`Ctrl` + `s` 를 생활화 합시다.
    앞에 공백을 4칸 넣어도 됩니다.
```

`Ctrl` + `s` 를 생활화 합시다.

​    앞에 공백을 4칸 넣어도 됩니다.



### 4. 목록(Lists)

#### 순서 없는 목록(Unordered)

```
* 오는데 순서 있지만
- 가는데 순서 없다
  * 오는데 순서 있지만
  - 가는데 순서 없다
  	* 오는데 순서 있지만
  	- 가는데 순서 없다
```

* 오는데 순서 있지만
* 가는데 순서 없다
  - 오는데 순서 있지만
  - 가는데 순서 없다
  	+ 오는데 순서 있지만
  	+ 가는데 순서 없다
#### 순서 있는 목록(Ordered)

```
1. 순
1. 서
   1. 순
   1. 서
```

1. 순
1. 서
   1. 순
   2. 서



### 5. 인용문(Blockquotes)

```
코난 오브라이언이 말하길:

> 가장 걱정하던 일이 실제로 일어나는 것만큼
> 우리를 더 자유롭게 만드는 일은 찾기 힘듭니다.
```

코난 오브라이언이 말하길:

> 가장 걱정하던 일이 실제로 일어나는 것만큼
> 우리를 더 자유롭게 만드는 일은 찾기 힘듭니다.



## 4. 첨부

### 1. 이미지(Images)

```
![홍인표](/images/busan.png "주석: 부산에서")

![Image of Yaktocat](https://octodex.github.com/images/yaktocat.png "Tooltip: Yaktocat")

<img src="/path/to/img.jpg" width="450px" height="300px" title="px(픽셀) 크기 설정" alt="RubberDuck"></img><br/>

<img src="/path/to/img.jpg" width="40%" height="30%" title="px(픽셀) 크기 설정" alt="RubberDuck"></img>
```

![홍인표](Markdown.assets/busan.jpg "툴팁:부산에서")



![Image of Yaktocat](https://octodex.github.com/images/yaktocat.png "Tooltip: Yaktocat")



### 2. 링크(Links)

```
http://github.com/hinpyo
[홍인표의 깃허브](http://github.com/hinpyo "여기도 주석 가능")
```

http://github.com/hinpyo
[홍인표의 깃허브](http://github.com/hinpyo "여기도 주석 가능")





# GitHub Flavored Markdown Syntax



## 1. 문단 제목(Headers)

```
제목 h1 태그
===
제목 h2 태그
---
```

제목 h1 태그
===
제목 h2 태그
---



## 2. 수평선(Horizontal Rules)

```
<hr>
```

<hr>



## 3. 본문

### 1. 강조(Emphasis)

```
***볼드와 이탤릭 동시적용***
~~취소선(Strikethrough)~~
<del>취소선(Strikethrough)</del>
<u>밑줄</u>
<span style="color:red">빨간 글씨입니다.</span>
<span style="color:#ff00ff">인표는 귀엽다(?)</span>
```

***볼드와 이탤릭 동시적용***
~~취소선(Strikethrough)~~
<del>취소선(Strikethrough)</del>
<u>밑줄</u>
<span style="color:red">빨간 글씨입니다.</span>
<span style="color:#ff00ff">인표는 귀엽다(?)</span>



### 2. 문법 강조(Syntax highlighting)

- 코드블럭 사용 + 언어 지정

```python
​```Python
def foo():
    if not bar:
        return True
​```
```

- 앞에 공백 4개 넣기(indent code by  four spaces) 또는 tab 넣기

```
  function fancyAlert(arg) {
      if(arg) {
        $.facebox({div:'#foo'})
      }
    }
```



### 3. 순서 없는 목록(Unordered Lists)

```
+ 이것도 되지롱
```

+ 이것도 되지롱



### 4. 할 일 목록(Task Lists)

```
- [x] 이거슨 완료한 일이여
- [ ] 이거슨 끝도 없는 남은 일이여
```

- [x] 이거슨 완료한 일이여
- [ ] 이거슨 끝도 없는 남은 일이여



### 5. 마크다운 서식 무시

```
\# 날 무시하지 마!
```

\# 날 무시하지 마!



## 2. 첨부

### 1. 표(Tables)

- `-`(hyphens)는 열의 제목(column's header)을 만들 때 사용하며 최소 3개 이상 있어야 한다.
- `-`(hyphens) 양 옆에 `:`를 붙여서 정렬 가능하다. (`:---`: 왼쪽 정렬,  `:---:`: 가운데 정렬, `---:`: 오른쪽 정렬)
- `|`(pipes)는 각 열을 구분할 때 사용하며 `|`(pipe) 양 옆에 공백문자를 넣어야 한다.
- 표 양 끝의 `|`(pipe)는 생략 가능하다.
- 표가 만들기 힘들다면 [표 생성기](https://www.tablesgenerator.com/markdown_tables "table generator")로

```
| 제목1 | 제목2 | 제목3 |
| :--- | :---: | ---: |
으어어 | 졸려서 | 죽을 것 같아요
진짜 | 레알 | 혼또니
```

| 제목1  | 제목2  |          제목3 |
| :----- | :----: | -------------: |
| 으어어 | 졸려서 | 죽을 것 같아요 |
| 진짜   |  레알  |         혼또니 |



### 2. 이모지(Emoji)

````
:book:
````

:book:

[참조: Emoji Cheat Sheet](https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md)



## 3. 링크(Links)

### 1. 문서 내 링크

```
규칙
1. 해당 제목의 서식 삭제
2. 공백을 `-`로 치환
3. 대문자를 소문자로
4. 특수문자와 이모지 삭제 eg. `.` `,` `(` `)` 등
5. 이모지가 있다면 양 끝 묶는::만 삭제 eg. :books: -> books

eg.📚 1.Today I Learned(Abc)
[맨 위로](#books-1today-i-learnedabc)
```

[맨 위로](#books-1today-i-learnedabc)



### 2. 문서 외 링크

```
상대경로는 아래와 같고 기준은 현재 README.md
링크 입력방법은 동일: [버튼내용](상대주소)

/ :루트
./ :현재 폴더
../ :상위 폴더
```



### 3. 내용 접기

- details 와 summary: summary가 부모인 details를 닫았다 열었다
- details 뒤에 open은 열린상태로 만들라는 의미
- markdown="1" 여기서 마크다운 문법을 사용한다는 의미
- div 는 가상의 레이아웃으로 꼭 안 써도 되는 듯

```
<details open>
<summary>접기/펼치기 버튼</summary>
<div markdown="1">

숨겨왔던 나의~

</div>
</details>


<details markdown="1">
<summary>접기/펼치기</summary>

짧게

</details>
```

<details open>
<summary>접기/펼치기 버튼</summary>
<div markdown="1">


숨겨왔던 나의~

</div>
</details>


<details markdown="1">
<summary>접기/펼치기</summary>


짧게

</details>



## 4. etc.

### 1. SHA references

- SHA-1 해시값을 직접 추가할 수 있다. 커밋 링크?

```
16c999e8c71134401a78d4d46435517b2271d6ac
mojombo@16c999e8c71134401a78d4d46435517b2271d6ac
mojombo/github-flavored-markdown@16c999e8c71134401a78d4d46435517b2271d6ac
```



### 2. Issue references within a repository

```
#1
mojombo#1
mojombo/github-flavored-markdown#1
```



### 3. Username @mentions



### 4. 섹션링크, 관계링크





# Typora Shortcut



## 1. 제목 서식

- `ctrl` + `=`: 제목 수준 올리기

- `ctrl` + `-`: 제목 수준 내리기
- `ctrl` + `0~6`: 제목 수준 변경 (0: 본문)
- 제목 맨 앞에서 `Backspace`: 제목 서식 삭제



## 2. 기타 서식

- `ctrl` + `]` or `tab`: 목록 수준 내리기
- `ctrl` + `[` or `shift` + `tab`: 목록 수준 올리기
- `ctrl` + `\`: 기타 서식 삭제
- `ctrl` + `shift` + ` : 인라인 코드로 만들기
- `win`  + `.`  or `:` + `영단어`: 이모지



## 3. 편집

- `ctrl` + `Z`: 실행 취소
- `ctrl` + `Y`: 실행 복귀
- `ctrl`+`shift`+`c`: Markdown으로 복사



## 4. 보기

- `ctrl` + `/`: 소스코드 모드

- `F8`: 포커스 모드
- `F9`: 타자기 모드
- `F11`: 전체화면 모드



