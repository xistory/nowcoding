# 문제-07
링크가 걸린 요소에 마우스를 갖다대면 노란색 배경이 나타나도록 구현해보세요.   

링크가 걸린 a태그요소는 회색바탕으로 되어있습니다. 여기에 마우스를 올려다놓으면 노란색 배경이 따라오도록 해야합니다.   

이를 위해 노란색 배경에 해당하는 요소를 새롭게 추가해줄겁니다.   
이 요소는 span태그로 만들어줍니다. span태그에 highlight 클래스를 추가해주면 필요한 태그가 완성됩니다. (style.css에서 highlight 클래스 부분을 참고해보세요)   

poiemaweb DOM 참고 : <https://poiemaweb.com/js-dom>

여기까지 완료되었다면 이제 각각의 a태그요소들에게 이벤트를 등록합니다.   
'mouseenter'이벤트를 등록합니다. 이벤트 함수명은 highlightLink로 만듭니다.   

highlightLink는 다음과 같은 동작을 합니다.   
해당 a태그요소의 위치와 크기를 구합니다. 구한 값을 앞서 만들었던 span태그요소의 위치와 크기에 넣어줍니다.   
(span태그요소에는 highlight 클래스가 지정되어 있기때문에 클래스 속성에 따라 알맞은 애니메이션이 동작합니다.)   

여기서 한가지 염두에 두어야할 것은 스크롤바입니다. 스크롤바가 내려가도 span태그요소는 알맞은 위치에 지정되어야합니다. 이를 위해 문서의 특성을 알 필요가 있습니다.   
참고1 : <https://opentutorials.org/module/904/7112>   
참고2 : <https://webisfree.com/2019-03-08/%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%ED%98%84%EC%9E%AC%EC%9D%98-%EC%8A%A4%ED%81%AC%EB%A1%A4%EB%B0%94-%EC%9C%84%EC%B9%98-%EA%B0%80%EC%A0%B8%EC%98%A4%EB%8A%94-%EB%B0%A9%EB%B2%95>   
참고3 (자바스크립트로 css접근하기) : <https://ibrahimovic.tistory.com/56>
