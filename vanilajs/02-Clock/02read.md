# 문제-02
index.html 을 브라우저에서 열면 시계가 나옵니다.   
현재 시각을 시침, 분침, 초침으로 나타내야합니다.   

html 요소를 살펴보면 hand클래스를 가진 div요소로 시침, 분침, 초침이 정의되어 있습니다.

setDate함수를 만들어서 1초마다 한번 씩 주기적으로 실행시켜줍니다.   
주기적인 함수 실행은 setInterval함수를 사용합니다.   
setInterval함수 참고 : <https://offbyone.tistory.com/241>

setDate함수에서는 다음과 같은 설정을 해줘야합니다.
- Date객체를 가져와서 현재 시, 분, 초를 구합니다.
- 현재 시, 분, 초에 해당하는 각도를 구합니다. 그 값을 각각 알맞은 요소의 (css) rotate프로퍼티값으로 지정해줍니다. (poiemaweb css 16장 참고)   
이를 위해서는 템플릿 리터럴 문법이 필요합니다.   
자바스크립트에서 css값에 접근하는 방법은 다음과 같습니다.   
ex) 해당요소.style.transform


# 필요한 문법(poiemaweb)
<https://poiemaweb.com/>  

CSS
- 16 트랜스폼

JavaScript
- 25 날짜와 시간을 위한 Date 객체

ECMAScript
- 2 템플릿 리터럴