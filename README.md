# HelloJQuery

## jQuery Library 사용법

### 다운로드해서 사용하기
1. http://www.jQuery.com 사이트에 접속해 최신 버전을 다운로드
2. <script>~</script> 태그 안에 src 속성으로 파일이 저장된 경로를 지정하여 사용
```
<head>
  <script src = "jquery-3.2.1.min.js"></script>
 </head>
```

### 웹에 접속해서 사용하기

```
<head>
   <script src="http://code.jQuery,com/jQuery-3.2.1.min.js"></script>
</head>
```

## 제이쿼리 코드 구조

|선택자 형식 | jQuery 코드 |
|:---:|:---|
|요소 선택자| $("p").hide(); |
|.class 선택자| $(".c1").hide(); |
|#id 선택자 | $("#oh").hide();|
|첫번째 요소| $("p:first").hide();|
|속성 선택자| $("[href]")|
|모든 선택자| $("*").hide();|
|자기 자신| $(this).hide();|
