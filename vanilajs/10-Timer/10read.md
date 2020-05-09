# 문제10
카운트다운 프로그램을 만들어봅시다.   
아래 그림에서 상단에 있는 메뉴를 누르면 그에 해당하는 타이머가 동작합니다.   
남은 시간(실시간)과 끝나는 시간이 표시됩니다.

<img src="https://github.com/xistory/nowcoding/blob/master/vanilajs/img/10-1.png" width="450px" height="300px"></img><br/>


이번 프로젝트에서는 Date 객체와 Math 객체를 많이 활용합니다.    
(poiemeaweb 자바스크립트 24, 25장)     

script 부분을 별도의 파일로 분리하겠습니다. scripts.js 파일에 작성합니다.   

1. 먼저 입력받은 시간만큼 카운트하는 timer 함수부터 만들어봅시다.   
시간은 '초'로 주고받을 것이고, 단위는 밀리세컨즈(ms)입니다.   
(이는 Date.now() 함수가 밀리세컨즈 단위로 동작하기 때문)   
setInterval 함수와 Date 객체, Math 객체를 활용해서 1초마다 갱신되는 카운터를 만들어봅시다.   
적절한 부분에 clearInterval을 해주는 것도 잊지맙시다.   
setInterval 참고 : <https://offbyone.tistory.com/241>   
아직 화면에 표시해줄 필요는 없고 콘솔에서 제대로 동작하는지 확인해봅시다.   

2. 남은 시간을 화면에 표시해주는 displayTimeLeft 함수와   
끝나는 시간을 화면에 표시해주는 displayEndTime 함수를 만들어봅시다.   
'분:초' 형식으로 화면에 표시해줍니다.   
프로그램 실행 중 동적으로 변하는 문자열을 구현해야하기때문에 템플릿 리터럴을 사용합니다.   
'초'를 표시해줄 때 한가지 유념해야할 미션이 있는데, 10초 이하일 때에는 초 앞에 0을 붙여줘야한다는 것입니다. 이는 자리수를 지켜주기 위해서입니다. 예를 들어,   
11, 10, 09, 08, 07, 06 …    
이런 식으로 카운트되도록 구현합시다.

3. 이제 timer 함수를 동작시키는 startTimer 함수를 만들어서, 상단의 버튼들에 각각 이벤트 핸들러로 등록해줍니다.(‘click’이벤트)   
상단최우측에 있는 form은 '분'단위로 시간을 입력해서 카운트해주도록 구현해봅시다. form 태그는 ‘submit’ 이벤트로 등록해주는데, 페이지가 다시 로드되는 것을 막기 위해 e.preventDefault() 함수를 적어줍시다.   
form 이벤트 참고 : <https://poiemaweb.com/js-event#91-eventpreventdefault>   
