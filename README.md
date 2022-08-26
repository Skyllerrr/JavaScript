# Egoing - JavaScript

## JavaScript 기본 (실행방법과 실습환경)
<br>

### [코드 작성과 실행]</br>

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8"/>
    </head>
    <body>
        <script>
            alert('Hello world');
        </script>
    </body>
</html>
```
![result](https://s3-ap-northeast-1.amazonaws.com/opentutorialsfile/module/532/1498.gif)

### 코드 script는 웹브라우저에게 지금부터는 자바스크립트 코드이기 때문에 이 코드를 해석 할 때는 자바스크립트의 문법에 따라서 해석해서 실행하라고 알려주는 구문(태그)다.<br> 
### <u>alert('Hello world')</u>는 경고창에 Hello world라는 문구를 출력하라는 일종의 명령이다. <br>script는 자바스크립트 구간이 끝났기 때문에 이 후부터 나타나는 코드는 HTML의 문법으로 <br>해석하라고 브라우저에게 알려주는 것이다.
<br>
<br>
<br>

### [크롬 개발자 도구 - 콘솔 사용법]</br>

<br>
크롬 개발자도구(f12)를 킨 후, console창에서는 html문구 필요없이 그대로 JavaScript내용을
사용할 수 있다.

<br>
<br>
<br>

### [주석]

<br>

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title></title>
</head>
<body>
<script type="text/javascript">
    /*
        여러줄
        여러줄
    */
   
    // 실습용 코드 입니다.
    alert(1+2); // 3입니다.
</script>
</body>
</html>
```
이와 같이 /* */를 사용하게 되면 안에 들어있는 모든 <br>내용들은 주석처리가 된다. (여러줄도 가능) <br>
기본적으로는 주석을 //표시로 나타내며 다음과 같은 <br>예시코드로 alert(1+2); 에 대한 설명과 답을 사용자가 주석처리로 말해줄 수도 있다.