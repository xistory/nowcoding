sounds 파일 다운로드 : <https://drive.google.com/open?id=1Q-8aYuyLWM2UcCDnTzRpad5we-Ub14hA>

# 문제-01
index-START.html 파일을 브라우져에서 열어봅니다.   
키보드에서 A, S, D, F, G, H, J, K, L 키를 눌렀을 때,   
- 해당 이미지가 연주하는 이미지로 바뀌고, (키를 때었을 때는 다시 원래 이미지로 돌아와야함)
- 키에 해당하는 소리가 연주되어야합니다.

연주하는 이미지는 css파일에서 playing클래스로 이미 작성되어있습니다.   
DOM에서 key클래스로 요소를 꺼낸 다음 playing클래스를 추가해주면 됩니다.   

두 가지 함수를 작성해서 addEventListener로 이벤트를 등록해줍니다.

1. 첫번째 함수는 playSound 입니다. window전역객체에 'keydown' 이벤트 발생 시 호출됩니다.   
DOM에서 해당하는 audio요소와 key요소를 선택합니다. (어트리뷰트 셀렉터, 템플릿 리터럴 사용)   
key요소에 playing클래스를 추가해줍니다.   
오디오를 연주해줍니다. (currentTime은 0으로 설정하고, play() 사용)   

playSound 함수는 addEventLisener 방식으로 window 전역객체에 바인딩해줍니다.

audio 태그 관련 참고 : <https://webisfree.com/2017-09-07/html5-audio-%ED%83%9C%EA%B7%B8-%EC%82%AC%EC%9A%A9-%EC%98%88%EC%A0%9C%EB%B3%B4%EA%B8%B0>   


2. 두번째 함수는 removeTransition 입니다.   
playSound에서 붙여주었던 playing클래스를 제거해줍니다.

removeTransition 함수는 각각의 key마다 모두 addEventListener 방식으로 바인딩해주어야합니다. 따라서 DOM으로 각각의 key들을 꺼내서 모두 배열에 집어넣은 후 그 배열에 forEach문으로 이벤트를 등록해줍니다.

transitionend 이벤트 : <https://mber.tistory.com/6>




# 필요한 문법
<https://poiemaweb.com/>   
CSS
- 2 셀렉터
- 14 트랜지션

JavaScript
- 28 배열
- 29 배열 고차함수
- 30 DOM, 32 이벤트

ECMAScript
- 2 템플릿 리터럴

