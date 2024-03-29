# ch 6. HTML 핵심 정리

# 01. 핵심 요소 정리

# `<div></div>` : 블록(상자) 요소

특별한 의미가 없는 구분을 위한 요소(division).  기본적으로 레이아웃을 작업 할때 주로 사용하는 것

여기를 어떻게 구분하지 라고 생각이 든다면 div를 사용

```html
<div>
	<h1>오늘의 날씨</h1>
	<p>중부 집중호우, 남부는 열대야, 12호 태풍 북상중...</p>
	<img src="img/weather.jpg" alt="12호 태풍" />
</div>
```

위와 같이 여러가지 개념을 한데 묶을때 보통 많이 사용

# `<h1></h1>` : 블록(상자) 요소

제목(heading)을 의미하는 요소. heading은 h1~h6까지 존재하며, 숫자가 커질수록 크기가 작아진다.

# `<p></p>` : 블록 상자 요소

문장(paragraph)을 의미하는 요소. 

글자를 다루고 있지만, 문장을 의미 하기 때문에 블록 요소로 구성되어 있다는 점을 명심

# `<img />` : 인라인 요소

이미지를 삽입하는 태그, 속성과 값이 강제되는 **빈 태그**로 필수 속성에는 src(source)와 alt(alternate)값이 존재한다.

# `<ul></ul>` : 블록(상자) 요소

순서가 필요없는 목록의 집합을 의미(Unorderd list), ul태그 안에는 li 태그가 반드시 하나는 들어 있어야한다.

# `<li></li>` : 블록(상자) 요소

목록 내 각 항목(list item)으로 `<ul></ul>` 의 자식 요소로 구성된다.

# `<a></a>` : 인라인(글자) 요소

다른/같은 페이지로 이동하는 하이퍼 링ㅜ크를 지정하는 요소로, anchor의 약자를 의미한다.

a 태그는 다른 페이지로 이동하는 특성 상, `href` 속성을 넣는 것을 강제한다.

- `target` : _blank를 입력할 경우 링크된 페이지가 어디에 표시될지 명시하는 속성

# `<span></span>` : 인라인(글자) 요소

특별한 의미가 없는 구분을 위한 요소, 특정 문자에 구분을 통하여 css를 입히고 싶을 경우 사용됨

# `<br>` : 인라인 요소

줄바꿈(break)을 의미하는 요소

# `<input />` :  인라인이면서 블록 요소(inline-block)

인라인 요소이긴 하지만, 상자가 가지고 있는 몇가지 요소를 가짐

- 가로/세로의 크기를 가질수 있으며
- 상하좌우 여백을 가질수 있음
- 

하지만 기본적으로 인라인이기 때문에 ************수평************으로 누적되게 됨

또한 빈 타입이기 때문에 속성을 사용하는 것을 강제

## input 태그에 주로 사용되는 속성

`type` 어떤 형태의 입력 값을 받을 지, 지정 하는 속성

또한 `value` 속성이 존재하는데, 사용자에게 데이터를 입력 받기 전에 미리 입력 되어있는 값을 지정 가능하다.

`placeholder`는 사용자가 입력할 값의 ******힌트******를 보여주는 속성 값이다.

`disabled` 는 입력 요소 비활성화 한 값으로, 이 속성은 값을 별도로 입력하지 않고, 선언 하는 것 만으로 효력을 발위하게 된다.

## - input 태그 type의 속성 값(일부 내용은 html5에서 지원)

- text : input 창에 입력되는 내용이 글자인 것을 의미
- checkbox : 체크박스(checkbox)를 정의함
    - `checked` 라는 속성을 통하여, 미리 체크된 상태로 만들 수 있음
- color : 색을 선택할 수 있는 입력 필드(color picker)를 정의함
- date : 날짜를 선택할수 있는 필드를 정의함(year, month, day)
- datetime-local : 날짜와 시간을 선택할 수 있는 입력 필드를 정의함(year, month, day, hour, minute)
- email : 이메일 주소를 입력할 수 있는 입력 필드를 정의함
- file : 업르드할 파일을 선택할 수 있는 입력 필드와 “파일 선택” 버튼을 정의함
- hidden : 사용자에게는 보이지 않는 숨겨진 입력 필드를 ㅓㅈㅇ의함
- image : 제출 버튼(submit button)으로 사용될 이미ㅣㅈ를 정의함
- month : 날짜를 선택할 수 있는 입력 필드를 정의함
- number : 숫자를 입력할 수 있는 입력필드를 정의함
- password : 비밀번호를 입력할 수 있는 입력 필드를 정의함
- radio : 라디오 버튼(radio button)을 정의함. 동일한 `name` 속성(그룹명으로 사용됨)에서 하나만 선택이 가능한 형태로 사용된다
    
    ```html
    ...
    	<label>
    		<input type="radio" name="fruits" /> apple
    	</label>
    	<label>
    		<input type="radio" name="fruits" /> banana
    	</label>
    ```
    
- range : 슬라이드 바를 조정하여, 범위 내의 숫자를 선택할 수 있는 입력 필드를 정의함
- reset : 리셋 버튼(reset button)을 정의함
- search : 검색어를 입력할 수 있는 텍스트 필드를 정의함
- submit : 제출 버튼 (submit button)을 정의함
- tel : 전화번호를 입력할수 있는 입력 필드를 정의함
- text : type 속성의 기본값으로 한줄로 된 텍스트 필드를 정의함
- time : 시간을 선택할 수 있는 입력 필드를 정의함(hour, minute)
- url : url 주소를 입력할수 있는 입력필드를 정의함
- week : 날짜를 선택할수 있는 입력 필드를 정의함

# `<label></label>` : 인라인(글자) 요소

라벨의 기능을 수행, 둘러싼 내용의 특정 라벨을 붙이는 형태로 사용된다

# `<table>` : 테이블 요소

표 요소로, 행(row)와 열(column)의 부모 요소로 사용되며, <table> 요소의 경우에는 인라인, 블록에 포함되지 않는 별도로 구분되는 요소이다.

(크게 보면 블록 요소)

******************행이 먼저******************라는 것을 반드시 기억 할 필요가 있음

## <tr></tr> : 행(테이블 요소)을 지정하는 요소 (table row)

## <td></td> : 열(테이블 요소)를 지정하는 요소(table data)