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
            console.log('Hello world');
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
    console.log(1+2); // 3입니다.
</script>
</body>
</html>
```
이와 같이 /* */를 사용하게 되면 안에 들어있는 모든 <br>내용들은 주석처리가 된다. (여러줄도 가능) <br>
기본적으로는 주석을 //표시로 나타내며 다음과 같은 <br>예시코드로 alert(1+2); 에 대한 설명과 답을 사용자가 주석처리로 말해줄 수도 있다.

<br>
<br>
<br>

## 숫자와 문자
<br>

### [수의 표현]

```javascript
console.log(1 + 1); // 결과 : 2
console.log(1.2 + 1.3); // 결과 : 2.5
```
자바스크립트에서는 큰따옴표나 작은따옴표가 붙지 않은 숫자는 숫자로 인식한다.

<br>
<br>
<br>

### [수의 연산]

```javascript
Math.pow(3,2);       // 9,   3의 2승 
Math.round(10.6);    // 11,  10.6을 반올림
Math.ceil(10.2);     // 11,  10.2를 올림
Math.floor(10.6);    // 10,  10.6을 내림
Math.sqrt(9);        // 3,   3의 제곱근
Math.random();       // 0부터 1.0 사이의 랜덤한 숫자
```
예를 들어, <u>Math.round(100 * Math.random());</u>은 랜덤한 숫자에 100을 곱한 후에 반올림을 하여 소수점을 없앤 정수값의 결과가 나온다.

<br>
<br>
<br>

### [문자의 표현]

```javascript
console.log('coding everybody');
console.log("coding everybody");

console.log('egoing\'s coding everybody');

typeof 1 // 결과 : number
typeof "1" // 결과 : string
```
문자형식으로 만들때는 작은 따옴표와 큰 따옴표끼리의 묶음으로 나타낼 수 있는데, 3번째 코드와 같이 <br>작은 따옴표 안에 작은 따옴표가 부득이하게 들어갈 때는 \ (역슬래쉬)를 붙여 구분하여 문자로 만들 수 있다.
<br>
<br>
typeof 라는 명령어로 어떠한 형태를 가지는지 알 수 있다.

<br>
<br>
<br>

### [문자의 연산]

```javascript
console.log("coding" + " everybody");

console.log(1+1); // 결과 : 2
console.log("1"+"1"); // 결과 : "11"

console.log("coding everybody").length; // 결과 : 16
console.log("coding everybody".indexOf("c")); // 결과 : 0
```
문자끼리 합쳐서 결과를 출력하기 위해선 + 기호로 만들 수 있다.

<br>
다음 코드는 숫자끼리 합친 결과와 문자끼리 합친 결과이다.

<br>
.length 메소드는 문자의 길이 즉, 개수를 파악하여 출력해주는 결과이다. <br>
.indexOf() 메소드는 해당 인덱스안에 찾고 싶은 문자를 적어주면, 몇 번째에 존재하는지 출력해주는 결과이다.

<br>
<br>
<br>

## 변수
<br>

### [변수의 사용법]

```javascript
var a = 1;
console.log(a + 1); // 결과 : 2

var first = "coding";
console.log(first + " everybody"); // 결과 : coding everybody

var a = 'coding', b = 'everybody';
console.log(a); // 결과 : coding
console.log(b); // 결과 : everybody
```
순서대로 a라는 변수에 1을 더하면서 결과가 2로 출력이 된다. <br> 
first라는 변수에 everybody라는 문자열을 더하면서 결과가 coding everybody로 출력이 된다. <br>
a라는 변수와 b라는 변수에 각각 coding, everybody라는 문자열을 정의하고 각각 출력하게 된다.

<br>
<br>
<br>

### [변수의 효용]

```javascript
var a = 100;
a = a + 10;
console.log(a);

a = a / 10;
console.log(a);

a = a - 10;
console.log(a);

a = a * 10;
console.log(a);
```
a라는 변수를 지정하고 100의 숫자 데이터를 넣는다. 변수에 10을 더해 그 결과를 a에 다시 넣게되면 출력값은 110이 된다. <br>이후, 계속된 연산을 하게 되면 해당 연산에 대한 출력값이 결과에 맞게 나온다.