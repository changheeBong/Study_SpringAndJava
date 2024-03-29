## JSON의 특징
### JSON은 다음과 같은 특징을 가집니다.
1. JSON은 자바 스크립트를 확장하여 만들어졌습니다.
2. JSON은 자바스크립트 객체 표기법을 따릅니다.
3. JSON은 사람과 기계가 모두 읽기 편하도록 고안되었습니다.
4. JSON은 프로그래밍 언어와 운영체제에 독립적입니다.

## JSON 표준
JSON은 2009년에 더글라스 크록포드(Douglas Crockford)가 처음으로 규정하였습니다. <br>
현재 JSON은 RFC 7159와 ECMA-404라는 두 개의 경쟁 표준에 의해 규정되고 있습니다. <br>
ECMA 표준에서는 문법만 정의할 정도로 최소한의 정보만 정의되어 있으며, RFC 표준은 문법 및 보안에 관련된 사항까지 일부 제공하고 있습니다.
<br><br>
JSON 표기법과 프로그래밍 언어별 지원 라이브러리에 대한 더 자세한 사항은 다음 링크를 참고하면 됩니다. <br>
## XML 이란?
XML은 EXtensible Markup Language의 약자입니다. <br>
이러한 XML은 HTML과 매우 비슷한 문자 기반의 마크업 언어(text-based markup language)입니다. <br>
이 언어는 사람과 기계가 동시에 읽기 편한 구조로 되어 있습니다. <br><br>

XML은 HTML처럼 데이터를 보여주는 목적이 아닌, 데이터를 저장하고 전달할 목적으로만 만들어졌습니다. <br>
또한, XML 태그는 HTML 태그처럼 미리 정의되어 있지 않고, 사용자가 직접 정의할 수 있습니다. <br> <br>

## JSON과 XML의 공통점
1. 둘 다 데이터를 저장하고 전달하기 위해 고안 되었습니다.
2. 둘 다 기계뿐만 아니라 사람도 쉽게 읽을 수 있습니다.
3. 둘 다 계층적인 데이터 구조를 가집니다.
4. 둘 다 다양한 프로그래밍 언어에 의해 파싱될 수 있습니다.
5. 둘 다 XMLHttpRequest 객체를 이용하여 서버로부터 데이터를 전송받을 수 있습니다.

## JSON과 XML의 차이점
하지만 JSON과 XML은 다음과 같은 차이점도 가지고 있습니다.
1. JSON은 종료 태그를 사용하지 않습니다.
2. JSON의 구문이 XML의 구문보다 더 짧습니다.
3. JSON의 데이터가 XML데이터보다 더 빨리 읽고 쓸 수 있습니다.
4. XML은 배열을 사용할 수 없지만, JSON은 배열을 사용할 수 있습니다.
5. XML은 XML파서로 파싱되며, JSON은 자바스크립트 표준 함수인 eval() 함수로 파싱됩니다.

## JSON의 사용 범위
xml 문서는 XML DOM(Document Object Model)을 이용하여 해당 문서에 접근합니다. <br>
하지만 JSON은 문자열을 전송받은 후에 해당 문자열을 바로 파싱하므로, xml보다 더욱 빠른 처리 속도를 보여줍니다. <br>
따라서 HTML과 자바스크립트가 연동되어 빠른 응답이 필요한 웹 환경에서 많이 사용되고 있습니다. <br>

하지만 JSON은 전송받은 데이터의 무결성을 사용자가 직접 검증해야 합니다. <br>
따라서 데이터의 검증이 필요한 곳에서는 스키마를 사용하여 데이터의 무결성을 검증할 수 있는 XML이 아직도 많이 사용되고 있습니다. <br>
## JSON 문법
JSON은 자바스크립트의 객체 표기법에서 리터럴(literal)과 프로퍼티(property)를 표현하는 방법만 가져와서 사용합니다. <br> 
따라서 JSON데이터는 모양과 규칙이 매우 단순합니다. <br>
그로 인해 브라우저 영역에서도 쉽고 빠르게 그 의미를 해석할 수 있으며, 다른 프로그래밍 언어에서도 구현하기 쉽습니다. <br>

## 리터럴(literal)
리터럴(literal)은 변수와 다르게 해석되는 값 그자체를 의미합니다. <br>
변수(variable)란 데이터(data)를 저장할 수 있는 메모리 공간을 의미하며, 그 값이 변경될 수 있습니다. <br>

## 객체(object)
객체란 실생활에서 우리가 인식할 수 있는 사물로 이해할 수 있습니다. <br>
JSON에서 객체란 이름(name)과 값(value)으로 구성된 프로퍼티(property)의 정렬되지 않은 집합입니다.

## JSON 구조
json은 자바스크립트의 객체 표기법으로부터 파생된 부분 집합입니다. <br>
따라서 json 데이터는 다음과 같은 자바스크립트 객체 표기법에 따른 구조로 구성됩니다.

1. JSON 데이터라는 이름과 값의 쌍으로 이루어집니다.
2. JSON 데이터는 쉼표(,)로 나열됩니다.
3. 객체(OBJECT)는 중괄호({})로 둘러쌓아 표현합니다.
4. 배열(ARRAY)은 대괄호([])로 둘러쌓아 표현합니다.

## JSON 데이터
JSON 데이터는 이름과 값의 쌍으로 구성됩니다. <br>
이러한 JSON 데이터는 데이터 이름, 콜론(:), 값의 순서로 구성됩니다. <br>
### 문법
"데이터이름" : 값

-----------------------
json은 경략 데이터 교환 형식으로, 인간이 읽고 쓰기 쉽고, 기계가 분석하고 생성하기도 쉽습니다. <br>
특히 웹 어플리케이션에서 데이터 전송과 저장을 위한 표준 포맷으로 널리 사용됩니다.

json은 키-값 쌍으로 이루어진 객체와 배열, 문자열, 숫자, 불리언(true/false)값과 null값을 표현할 수 있습니다. <br>
JSON포맷은 일반 텍스트로 작성되며 파일 확장자는 .json으로 표시됩니다.

아래는 간단한 JSON 객체의 예시입니다.
```json
{
    "name" : "John",
    "age" :30,
    "city : "New York"
}
```
이 객체는 name age city 세 개의 키를 가지며, 각각의 값은 문자열 "jhon",숫자 30, 문자열 "new york"입니다. <br>
JSON은 다른 프로그래밍 언어와 상호운용성이 좋습니다. 예를 들어, 자바스크립트엣 JSON 객체를 파싱하여 객체 또는 배열로 변활할 수 있으며, 파이썬에는 json 모듈을 사용하여 JSON 데이터를 읽고 쓸 수 있습니다. <br>

JSON은 xml에 비해 문법이 간단하며, 더 가볍고 빠르게 처리할 수 있습니다. 그러나 json은 xml보다 표현력이 떨어지며, 메타데이터를 표현하기에 적합하지 않습니다. <br>
JSON은 현재 웹에서 가장 많이 사용되는 데이터 교환 형식 중 하나이며, 다양한 프로그래밍 언어와 기술에서 널리 사용됩니다. <br>
JSON 데이터를 생성하고 가공하는 방법은 다양합니다. 여기에서는 일반적으로 사용되는 몇 가지 방법을 설명하겠습니다.

1. 객체 리터럴 사용하기
JavaScript 에서 JSON 데이터를 생성하는 가장 간단한 방법은 객체 리터럴을 사용하는 것입니다. <br>
객체 리터럴은 중괄호 ({})안에 키-값 쌍으로 데이터를 정의하는 방법입니다.
`ver person = {"name":"John","age":30,"city":"New York"};`
   
2. JSON.stringify() 사용하기
JavaScript에서는 JSON.stringfy() 함수를 사용하여 객체를 JSON 문자열로 변환할 수 있습니다. <br>
예를 들어:
```javascript
var person = {"name", "John", "age":30, "city": "New York"};
var jsonStr = JSON.stringify(person);
console.log(jsonStre); // 결과 : {"name":"John","age":30,"city":"New York}
```
3. JSON.parse() 사용하기
JSON 문자열을 JavaScript 객체로 변환하려면 JSON.parse() 함수를 사용합니다.
```javascript
var jsonStr = '{"name":"John","age":30,"city":"New York"}';
var person = JSON.parse(jsonStr);
console.log(person.name); // 결과 : "John"
```

4. REST API에서 데이터 가져오기
REST API는 JSON 형식의 데이터를 제공하는 것이 일반적입니다. <br>
JavaScript에서는 XMLHttpRequest 객체나 fetch API를 사용하여 서버에서 데이터를 가져올 수 있습니다.
```javascript
fetch('https://example.com/api/person/1')
.then(response => response.json())
.then(data => console.log(data.name));
```
이처럼 JSON데이터를 생성하고 가공하는 방법은 다양합니다. 어떤 방법을 선택하느냐에 따라 데이터 생성과 가공의 효율성과 편리성이 달라질 수 있습니다.

 
