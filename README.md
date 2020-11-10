# HelloJQuery

## jQuery Library 사용법

### 다운로드해서 사용하기
1. http://www.jQuery.com 사이트에 접속해 최신 버전을 다운로드
2. <script>~</script> 태그 안에 src 속성으로 파일이 저장된 경로를 지정하여 사용
```javascript
<head>
  <script src = "jquery-3.2.1.min.js"></script>
 </head>
```

### 웹에 접속해서 사용하기

```javascript
<head> 
   <script src="http://code.jQuery,com/jQuery-3.2.1.min.js"></script>
</head>
```
## jQuery 코드 구조와 이벤트 처리

### 코드 구조

|선택자 형식 | jQuery 코드 |
|:---:|:---|
|요소 선택자| <u>$("p").</u>hide(); |
|.class 선택자| <u>$(".c1").</u>hide(); |
|#id 선택자 | <u>$("#oh").</u>hide();|
|첫번째 요소| <u>$("p:first").</u>hide();|
|속성 선택자| <u>$("[href]")</u>|
|모든 선택자| <u>$("*").</u>hide();|
|자기 자신| <u>$(this).</u>hide();|

### 이벤트 종류

|이벤트 | 메소드 |
|:---|:---|
|Browser Events| error, resize, scroll |
|Document Loading| load, unload, ready |
|Form Events|submit, focus, change, select, blur|
|Keyboard Events|keydown, keypress, keyup|
|Mouse Events|click, dbclick, mouseenter, mouseleave, mousedown, mouseup|

```javascript
$(document).ready(function(){
 $("p.q1").on("click", function(){
  $("span.q1").show();
 });
});
```

## CSS 스타일 처리

### CSS 스타일 변경

|메소드|설명|     예제    |
|:---|:---|---|
|addClass()| 하나 이상의 클래스 추가 |
|removeClass()| 하나 이상의 클래스 삭제 |
|toggleClass()| 클래스 추가 및 삭제를 반복적으로 수행 |
|css()| 스타일 속성을 설정하거나 반환 | $("p").css({"background-color" : "yellow" , "font-size" : "200%"});
|width()| 가로 크기 반환 ( padding, border, margin 제외) |
|height()| 세로 크기 반환 ( padding, border, margin 제외) |

#### 예제

```javascript
<head>
 <script src="jquery-3.2.1.min.js"></script>
 <script>
  $(document).ready(function () {
  var xWidth=100;
  var yHeight=100;
  $("div").on("click",function () {
   $(this).width(xWidth).addClass("box");
   $(this).height(yHeight).addClass("box");
   xWidth=xWidth-10;
   yHeight=yHeight-10;
   });
  });
 </script>
 <style>
   div {
    width: 100px;
    height: 100px;
    float: left;
    margin: 5px;
    background: yellow;
   }
   .box {
    background: red;
   }
 </style>
</head>
```

## 애니메이션 처리

| 메소드 |   설명   | 사용 |
|---|---|---|
|animate()| 크기 및 위치 변경 | $(선택자).animate(CSS속성 및 속성값 [,지속시간(slow,fast,100ms]) |
|show()| 선택한 요소 보여주기 | $(선택자).show("slow"); |
|hide()| 선택한 요소 숨기기 | $(선택자).hide("fast"); |
|toggle()| 선택한 요소 보여주거나 숨기기 반복 | $(선택자).toggle(1000)|
|stop()|애니메이션 효과 중지. fade, slide 메소드에 적용 |
|fadeIn(), fadeOut(), fadeToggle()| 선택한 요소를 서서히 보이게 하고, 사라지게 한다. |
|fadeTo()| 선택한 요소를 서서히 투명하게 나타냄. 투명도는 0.0~1.0으로 지정 | $(선택자).fadeTo("slow",0.5); |
|slideUp(), slideDown(), slideToggle()| 선택한 요소를 밀어 올리거나 내린다. |

## 메소드 체이닝

> 단일 구문 내에서 동일한 요소 선택자에 여러 기능의 메소드를 한꺼번에 적용

```javascript
$("p").on("click",function(){
 $("#red").css("color","red")
          .slideDown(2000)
          .slideUp(6000)
          .fadeTo("slow",0.3);
};
```

### jQuery 함수

```javascript
<script>
   function move(obj, time) {
     $(obj).stop().animate( {
         left:-350,
         top:0
     }, time);
   }
   function back(css) {
     $(css).stop().animate( {
         left:0,
         top:0
     });
   }
</script>

```





