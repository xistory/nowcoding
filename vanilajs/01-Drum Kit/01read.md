# 문제-01
index-START.html 파일을 브라우져에서 열어봅니다.   
키보드에서 A, S, D, F, G, H, J, K, L 키를 눌렀을 때,   
- 해당 이미지가 연주하는 이미지로 바뀌고, (키를 때었을 때는 다시 원래 이미지로 돌아와야함)
- 키에 해당하는 소리가 연주되어야합니다.

연주하는 이미지는 css파일에서 playing클래스로 이미 작성되어있습니다.   
DOM에서 key클래스로 요소를 꺼낸 다음 playing클래스를 추가해주면 됩니다.   

두 가지 함수를 작성해서 addEventListener로 이벤트를 등록해줍니다.

1. 첫번째 함수는 playSound 입니다. window전역객체에 'keydown' 이벤트 발생 시 호출됩니다.   
입력매개변수로 Event객체를 받습니다.   
DOM에서 해당하는 audio요소와 key요소를 선택합니다.   
key요소에 playing클래스를 추가해줍니다.   
오디오를 연주해줍니다. (play() 사용)   

2. 



# 필요한 문법
<https://poiemaweb.com/>

