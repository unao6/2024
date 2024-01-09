# 2024 HTML 학습장

<tag>contents</tag> : 시작태그, 종료태그로 구성
<tag> : 시작태그만 존재하는 경우. 빈 요소(Empty Element)
<tag attr="value"> Attribute(속성) : tag에 추가 정보
WYSIWYG : What you see is what you get. HTML은 지원되지 않음.
<!DOCTYPE HTML> HTML5 문서 형식 정의 : 출력할 웹 페이지의 형식을 브라우저에 전달
<html> 모든 HTML 요소의 부모요소. 웹페이지에 단 하나만 존재. <!DOCTYPE>만 예외

<head> HTML 문서의 설정. 메타데이터를 포함하기 위한 요소. 메타데이터 이외의 화면에 표시되는 일체의 요소를 포함시킬 수 없음. 콘텐츠와 상관 없는 정보들 (눈으로 확인되지 않음). / 추가정보, 타이틀, 파일import
<title> 문서의 제목. 브라우저의 탭에 표시됨.
<style> 스타일 정의
<link> 외부 리소스와 연계정보를 정의. 주로 CSS 파일 연계에 사용 <link rel="stylesheet" href="style.css">
<script> JavaScript 정의. src 어트리뷰트로 외부 javaScript 파일 로드도 가능 <script src="main.js"></script>
<meta> 메타 요소는 기타 메타데이터 정의에 사용. 메타데이터는 브라우저, 검색엔진(keywords) 등에 사용됨. 빈 요소.
<meta charset="utf-8"> 브라우저가 사용 할 문자셋 정의
검색엔진이 사용할 keywords 정의 <meta name="keywords" content="HTML, CSS, XHTML, JavaScript">
웹페이지의 설명을 정의 <meta name="description" content="Web tutorials on HTML and CSS">
웹페이지의 저자를 정의 <meta name="author" content="Goeun Choi">
웹페이지를 30초마다 새로고침 <meta http-equiv="refresh" content="30">

검색엔진에 노출되지 않는다 = 웹 세상에 존재하지 않는다. 따라서 html을 의미에 맞게 정확하게 사용하는 것이 아주 중요한 문제이다.

<body> HTML 문서의 내용을 표시. 메타데이터를 제외한 웹페이지를 구성하는 대부분의 요소가 body 요소 내에 기술된다.
<h1>...<h6> 제목 태그. 시멘틱 웹의 의미를 살려서 제목 이외에는 사용하지 않기. 검색엔진은 제목 태그를 중요한 의미로 받아들일 가능성이 큼
<b> bold체. 중요성의 의미는 없음
<strong> bold체. 중요성의 의미 있음. (Semantic)
<i> Italic체. 중요성의 의미 없음.
<em> emphasized text 지정. Italic체. 중요성의 의미 있음. (Semantic)
<small> 작은 글씨
<mark> 하이라이트 텍스트
<u> underlined 텍스트
<ins> inserted (added) 텍스트. 밑줄
<sub / sup> sub는 아래에 오도록, sup은 위에 오도록 쓰인 텍스트

<p> 단락 지정. 문단. 줄바꿈o
<br> 강제 줄바꿈.(enter) 빈 요소(종료 태그 없음)
&nbsp; 강제 공백. (space) (Non-Break Space). 엔터티 코드
<pre> preformatted (형식화된) text 지정. pre 태그 내의 content는 작성된 그대로 브라우저에 표시됨.
<hr> 수평 줄 삽입. 구분선. 빈 요소
<q> quotation(짧은 인용문) 지정. 브라우저는 인용부호(큰 따옴표/ quotation marks)로 q요소를 감싼다.
<blockquote> 긴 인용문 블록 지정. 브라우저는 요소를 들여쓰기 한다. css를 이용하여 다양한 style 적용 가능.

<a> anchor 태그. 하이퍼링크 기능을 담당
href 어트리뷰트는 이동하고자 하는 파일의 위치(경로)를 값으로 받는다. <a href="http://www.google.com">Visit Google!</a>
target 어트리뷰트는 링크를 클릭했을 때 윈도우를 어떻게 오픈할 지를 정한다.// Value: "_self" , "_blank"
현재 윈도우에서 오픈(기본값) target="_self"
새로운 윈도우나 탭에서 오픈 target="_blank"
blank를 사용해 외부 페이지를 오픈하는 경우, rel="noopener noreferrer"을 추가해 Tabnabbing 피싱공격에 대비할 것을 권장함.


<ul> 순서 없는 목록
<li></li>
<ol> 순서 있는 목록
<li></li>
type 어트리뷰트를 사용하여 순서를 나타내는 문자를 지정할 수 있다. // Value : "1", "A", "a", "I"(대문자 로마숫자), "i"(소문자 로마숫자)
start 어트리뷰트로 리스트의 시작 값을 지정할 수 있다.<ol start="3">
reversed 어트리뷰트로 리스트의 순서 값을 역으로 표현 가능.
<table> 표 만드는 태그. 요새는 주로 div를 사용하여 레이아웃을 구성함 // <tr>행. <th>행 내부의 제목 셀, <td>행 내부의 일반 셀
테이블 코드 생성기

<img> 웹페이지에 이미지 삽입
src 어트리뷰트 : 이미지 파일 경로
alt 어트리뷰트 : 이미지 파일이 없을 경우 표시되는 문장
width, height 어트리뷰트 : 이미지의 너비, 높이 (CSS에서 지정하는 것이 일반적)
<img src="assets/images/doug.jpg" alt="doug" width="100">
<img src="assets/images/doug.jpg" alt="이미지가 없습니다.">

<audio> 음악 파일. HTML5에서 추가. IE8 이하에서 사용 불가
src 어트리뷰트 : 음악 파일 경로
preload : 재생 전에 음악 파일을 모두 불러올 것인지 지정
autoplay : 음악 파일을 자동 재생 개시할 것인지 지정
loop : 음악을 반복할 것인지 지정
controls : 음악 재생 도구를 표시할 것인지 지정. 재생 도구의 외관은 브라우저마다 차이가 있음.
웹브라우저 별로 지원하는 음악 파일 형식이 다르다. (MP3 사용하기)
source 태그를 사용하여 파일 형식의 차이 문제를 해결할 수 있다. type 어트리뷰트는 생략이 가능하다.

<video> 동영상 파일. HTML5에서 추가. IE8 이하에서 사용 불가
src 어트리뷰트 : 동영상 파일 경로
poster : 동영상 준비 중에 표시될 이미지 파일 경로
preload : 재생 전에 동영상 파일을 모두 불러올 것인지 지정
autoplay : 자동 재생 개시할 것인지 지정
loop : 동영상을 반복할 것인지 지정
controls : 동영상 재생 도구를 표시할 것인지 지정. 재생 도구의 외관은 브라우저마다 차이가 있음.
width, height : 동영상의 너비, 높이 지정
audio 태그와 마찬가지로 파일 형식의 차이 문제가 발생할 수 있다. source 태그를 사용하여 해결할 수 있다. type 어트리뷰트는 생략이 가능하다. (MP4 사용하기)

<form> 사용자가 입력한 데이터를 수집하기 위해 사용.
- input, textarea, button, select, checkbox, radio button, submit button 등의 입력 양식 태그를 포함할 수 있음.
action 어트리뷰트 + URL 밸류 : 입력 데이터(form data)가 전송 될 URL 지정
method 어트리뷰트 + get/ post 밸류 : 입력 데이터(form data) 전달 방식 지정
- get과 post는 HTTP 프로토콜을 이용해서 사용자 입력 데이터를 서버에 전달하는 방식을 나타내며 HTTP request method라 한다.
<form action="http:// jsonplaceholder.typicode.com/users" method="get">
ID: <input type="text" name="id" value="아이디를 입력하세요"><br>
username: <input type="text" name="username" value="이름을 입력하세요"><br>
<input type="submit" value="제출">
</form>
<input> form 태그 중에서 가장 중요한 태그로 사용자로부터 데이터를 입력받기 위해 사용된다.
type 어트리뷰트로 다양한 종류를 구현할 수 있음. form 태그 내에 존재하여야 입력 데이터를 전송할 수 있으나, ajax를 사용할 시에는 form 태그 내에 존재하지 않아도 됨. 서버에 전송되는 데이터는 name 어트리뷰트를 key로, value 어트리뷰트를 값으로 하여 key=value의 형태로 전송됨.
- button, checkbox, color, date, datetime, datetime-local, email, file, hidden, image, month, number, password, radio, range, reset, search, submit, tel, text, time, url, week ........... <input type="date" name="birthday">

<select> 복수 개의 리스트에서 복수 개의 아이템을 선택할 때 사용. // <select> <option> <optgroup>
서버에 전송되는 데이터는 select 요소의 name 어트리뷰트를 key로, option 요소의 value 어트리뷰트를 값으로 하여 ken=value 형태로 전송됨.
<select name="cars1">
<option value="cars" selected>Cars</option>
<option value="volvo">Volvo</option>
<option value="saab" disabled>saab</option>
<option value="flat">Flat</option>
<option value="audi">Audi</option>
</select>

<textarea> 여러 줄의 글자를 입력할 때 사용
<textarea name="message" rows="10" cols="30">Write here</textarea>

<button> 클릭할 수 있는 버튼 생성.
<input type="button">과 유사하지만 input 태그는 빈 태그인 반면, button 태그는 그렇지 않아서 텍스트나 이미지 콘텐츠를 사용할 수 있음.
type 어트리뷰트는 반드시 지정하는 것이 바람직. 어트리뷰트 값으로 button, reset, submit을 지정할 수 있다.
<button type="button" onclick="alert('Hello World!')">Click Me!</button>
<input type="button" value="Click Me!" onclick="alert('Hello World!')">


<fieldset> 관련된 입력 양식들을 그룹화할 때 사용
<legend> fieldset 태그 내에서 사용되어야 하며 그룹화된 fieldset의 제목을 정의한다.

<div> 공간을 분할할 때 사용. 의미론적으로 아무 의미 없는 태그.
아래는 시멘틱 태그(IE에서 작동하지 않음.)
<header> 헤더
<nav> 내비게이션
<aside> 사이드에 위치하는 공간
<section> 본문의 여러 내용(article)을 포함하는 공간
<footer> 푸터
