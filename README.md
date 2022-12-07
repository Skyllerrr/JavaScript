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

<br>
<br>
<br>

## 비교
<br>

### [연산자]

연산자란 값에 대해서 어떤 작업을 컴퓨터에게 지시하기 위한 기호이다. <br>
예를 들어, "**a = 1**은 a라는 변수에 1이라는 값을 대입해준다"라는 뜻이다.

<br>
<br>
<br>

### [비교 연산자 (==와 ===)]

```javascript
alert(1==2) // 결과 : false
alert(1==1) // 결과 : true
alert("one"=="two") // 결과 : false 
alert("one"=="one") // 결과 : true

alert(1=='1'); // 결과 : true
alert(1==='1'); // 결과 : false
```
"=="은 양쪽의 값이 똑같으면 true, 아니면 false를 출력한다.

"==="와 "=="의 차이점은 양쪽의 값과 데이터 형식까지 모두 같으면 "==="를 사용하여 true를 출력하게 되며, <br> 데이터 형식을 생각하지 않아도 양쪽의 값이 같으면 "=="를 사용하여 true를 출력하게 된다.

<br>
<br>
<br>

### [===를 사용하자!]

```javascript
alert(null == undefined); // 결과 : true
alert(null === undefined); // 결과 : false
alert(true == 1); // 결과 : true
alert(true === 1); // 결과 : false
alert(true == '1'); // 결과 : true
alert(true === '1'); // 결과 : false
 
alert(0 === -0); // 결과 : true
alert(NaN === NaN); // 결과 : false
```
null과 undefined는 값이 없다는 의미의 데이터 형이다. <br>
null은 값이 없음을 명시적으로 표시한 것이고, undefined는 그냥 값이 없는 상태이다.

NaN은 0/0과 같은 연산의 결과로 만들어지는 특수한 데이터 형인데, 숫자가 아니라는 뜻이다.

따라서 null과 undefined, true와 1 등등 동등연산자 "=="는 숫자 1은 true로 간주하여 항상 true를 출력할 수 있지만, 일치 연산자 "==="는 데이터 형이 다르기 때문에 같은 데이터 형이 아닌 이상 항상 false가 나올 수 밖에 없다.

<a href="http://dorey.github.io/JavaScript-Equality-Table/">Link : ==와 ===의 차이점을 나타낸 표</a> ***[초록색칸은 true, 흰색칸은 false]***

<br>
<br>
<br>

### [부정과 부등호]

```javascript
"!="
console.log(1!=2); // 결과 : true
console.log(1!=1); // 결과 : false
console.log("one"!="two"); // 결과 : true
console.log("one"!="one"); // 결과 : false

">"
console.log(10>20); // 결과 : false
console.log(10>1); // 결과 : true
console.log(10>10); // 결과 : false

">="
console.log(10>=20); // 결과 : false
console.log(10>=1); // 결과 : true
console.log(10>=10); // 결과 : true
```
각각 부정(아니다)과 부등호(크다, 크거나 같다, 작다, 작거나 같다)에 관련된 출력 결과이다.

<br>
<br>
<br>

## 조건문
<br>

### [조건문이란?]

```JavaScript
if(true) {
    console.log('result : true');
}

if(false) {
    console.log('result : true');
}

if(true) {
    alert(1);
    alert(2);
    alert(3);
    alert(4);
}
alert(5);

if(false) {
    alert(1);
    alert(2);
    alert(3);
    alert(4);
}
alert(5);
```
처음 예시의 코드는 조건이 true인 코드만 result : true라는 문구가 출력이 되고, false 조건일때는 아예 출력이 되지 않는다.

두 번째 코드는 true 조건에서 alert을 사용하여 1부터 시작하여 확인 버튼을 누를 때 마다 2,3,4,5가 순서대로 출력되며, false 조건일때는 false 바깥쪽에 있는 5만 출력이 된다.

<br>
<br>
<br>

### [else와 else if]

if else
```JavaScript
//ex 1)

if(true){
    alert(1);
} else {
    alert(2);
}
// 결과 : 1

//ex 2)

if(false){
    alert(1);
} else {
    alert(2);
}
// 결과 : 2
```
else if
```JavaScript
//ex 1)

if(false){
    alert(1);
} else if(true){
    alert(2);
} else if(true){
    alert(3);
} else {
    alert(4);
}
// 결과 : 2

//ex 2)

if(false){
    alert(1);
} else if(false){
    alert(2);
} else if(true){
    alert(3);
} else {
    alert(4);
}
//결과 : 3

//ex 3)

if(false){
    alert(1);
} else if(false){
    alert(2);
} else if(false){
    alert(3);
} else {
    alert(4);
}
//결과 : 4
```
if, else if 안의 true 또는 false에 따라 결과값이 달라진다.

<br>
<br>
<br>

### [조건문의 응용]

```JavaScript
id = prompt('아이디를 입력해주세요.')
        if(id=='egoing'){
            alert('아이디가 일치 합니다.')
        } else {
            alert('아이디가 일치하지 않습니다.')
        }
```
코드를 실행하게 되면, prompt 명령어를 통해 아이디를 입력하라는 빈칸이 생성된다. <br> 입력한 아이디는 id안에 들어가게 되고, 이 id가 egoing이라고 입력하게 되면 아이디가 일치 한다고 출력이 되며, 다르면 아이디가 일치하지 않는다고 출력이 된다.

```JavaScript
id = prompt('아이디를 입력해주세요.');
        if(id=='egoing'){
            password = prompt('비밀번호를 입력해주세요.');
            if(password==='111111'){
                alert('로그인 하셨습니다.');
            } else {
                alert('비밀번호가 다릅니다.');
            }
        } else {
            alert('아이디가 일치하지 않습니다.');
        }
```
비밀번호도 마찬가지로 id가 일치한 경우에만 실행이 되며, 일치하지 않으면 아이디가 일치하지 않는다고 출력이 된다. <br> id가 일치한 경우, password를 111111로 입력하게 되면 로그인을 할 수 있으며, 다르면 로그인에 실패하게 되며 비밀번호가 다르다고 출력이 된다.

<br>
<br>
<br>

### [논리 연산자]

ex 1) &&
```JavaScript
id = prompt('아이디를 입력해주세요.');
        password = prompt('비밀번호를 입력해주세요.');
        if(id=='egoing' && password=='111111'){
            alert('인증 했습니다.');
        } else {
            alert('인증에 실패 했습니다.');
        }
```
위의 조건문의 응용 파트에서 아이디와 비밀번호를 입력하여 결과값을 출력하는 예제에서 &&를 이용하여 조건을 합친 후, 결과값을 나타낼 수도 있다.

ex 2) || 를 이용한 예제 개선
```JavaScript
id = prompt('아이디를 입력해주세요.');
password = prompt('비밀번호를 입력해주세요.');
if((id==='egoing' || id==='k8805' || id==='sorialgi') && password==='111111'){
    alert('인증 했습니다.');
} else {
    alert('인증에 실패 했습니다.');
}
```
or 연산자를 이용하여 id값이 egoing 이거나 k8805 이거나 sorialgi 일 때, password가 111111이면 인증을 할 수 있지만, id값이 셋 중 하나라도 일치하지 않게 되면 인증에 실패하는 결과값을 얻게 된다.

<br>
<br>
<br>

### [boolean의 대체제]

if 뒤에 boolean값 대신 if(0){alert(1);}이나, if(1){alert(1);}로 0이나 1처럼 숫자를 넣어서 쓸 수 있지만, 보통은 잘 사용하지 않는다.

<br>
<br>
<br>

## 반복문
<br>

### [반복문과 기본문법 - while]

while (조건){
    반복해서 실행할 코드
}

<br>
<br>
<br>

### [반복 조건]

```JavaScript
var i = 0;
// 종료조건으로 i의 값이 10보다 작다면 true, 같거나 크다면 false가 된다.
while(i < 10){
    // 반복이 실행될 때마다 coding everybody <br />이 출력된다. <br /> 줄바꿈을 의미하는 HTML 태그
    document.write('coding everybody <br />');
    // i의 값이 1씩 증가한다.
    i++
}
```

<br>
<br>
<br>

### [for문]

문법 - 
for(초기화; 반복조건; 반복이 될 때마다 실행되는 코드){
    반복해서 실행될 코드
}
```JavaScript
예제
for(var i = 0; i < 10; i++){
    document.write('coding everybody'+i+'<br />');
}
```

<br>
<br>
<br>

### [반복문의 제어]

```JavaScript
for(var i = 0; i < 10; i++) {
    if(i === 5) {
        break;
    }
    document.write('Coding everybody' + i + '<br>');
}
```
i = 0부터 시작해서 1씩 증가하는 반복문에서 i값이 5가 되었을 때, break를 사용하여 해당하는 결과값을 중간에 멈출 수 있다. 반대로, continue는 멈추지않고 계속 출력된다.

<br>
<br>
<br>

### [반복문의 중첩사용과 디버거]

```JavaScript
// 0부터 9까지 변수 i에 순차적으로 값을 할당        
for(var i = 0; i < 10; i++){
    // 0부터 9까지의 변수를 j의 값에 순차적으로 할당
    for(var j = 0; j < 10; j++){    
        // i와 j의 값을 더한 후에 출력
        // String은 숫자인 i와 j의 데이터 타입을 문자로 형태를 변환하는 명령이다. 
        // String()을 제거하고 실행해보면 의미가 좀 더 분명하게 드러날 것이다.
        document.write(String(i)+String(j)+'<br />');
    }
}
```

<br>
<br>
<br>

## 함수
<br>

### [함수란?]

```javascript
function numbering() {
    i = 0;
    while(i < 10){
        document.write(i);
        i += 1;
    }
}
numbering();
```