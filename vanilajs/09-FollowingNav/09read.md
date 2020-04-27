# 문제9
네비게이션 버튼에 마우스를 올려다놓으면 아래 그림과 같이 세부메뉴가 나타나도록 구현해봅시다.   
마우스를 떼어내면 세부메뉴도 다시 사라집니다.   
앞으로는 세부메뉴를 dropdown이라고 명명하겠습니다.

<img src="https://github.com/xistory/nowcoding/blob/master/vanilajs/img/09-1.png" width="450px" height="300px"></img><br/>

dropdown은 '내용'과 '바탕'으로 이루어져있습니다.   
'바탕'은 nav.top요소 아래의 div.dropdownBackground 요소가 담당합니다. (그림에서 하얀색 바탕을 의미)   
'내용'요소의 크기와 위치가 '바탕'요소에 지정되는 방법으로 동작합니다.   

1. 먼저 필요한 요소들을 선택해봅시다.   
네비게이션에 있는 3개의 trigger들을 선택합니다. ('About Me', 'Courses', 'Other Links'에 해당)   
querySelectorAll을 사용하여 한꺼번에 선택해서 triggers 변수에 넣습니다.   
다음으로 div.dropdownBackground 요소를 선택해서 background 변수에 넣습니다.   

2. 이벤트 등록을 해줍니다.   
총 2가지 이벤트를 각각의 trigger에 모두 등록해줍니다.   
- 마우스를 갖다대었을 때 : 'mouseenter'이벤트이고 이벤트 핸들러는 'handleEnter'함수와 연결해줍니다.   
- 마우스를 떼었을 때 : 'mouseleave'이벤트이고 이벤트 핸들러는 'handleLeave'함수와 연결해줍니다.   
각 이벤트 핸들러에 console.log로 메세지를 넣고 잘 동작하는지 확인해봅시다.   

이제 handleEnter 함수 내부를 구현해봅시다.   

3. 먼저 dropdown의 '내용'이 나타나도록 해봅시다. ('바탕'은 뒷  단계에서 구현합니다)   
해당 trigger에 'trigger-enter' 클래스와 'trigger-enter-active' 클래스를 추가해주면 화면에 나타납니다.    
css style을 살펴보면 trigger-enter는 display값을 block으로 바꿔주고,   
trigger-enter-active는 opaciry값을 1로 바꿔주는 것을 알 수 있습니다.   
(클래스를 2개로 나누어 만든 이유는 뒤에서 살펴보겠습니다)   
참고 : <https://poiemaweb.com/css3-display>   

4. dropdown의 '내용'이 잘 나타난다면 이제 '바탕'이 나타나도록 구현해봅시다.   
'바탕'이 '내용'위치에 나타나는 것은 뒤에서 하고 일단, 화면에 나타나도록 먼저 구현해봅시다.   
background에 'open' 클래스를 추가해줍니다.   
이제 trigger에 마우스를 갖다대었을 때 '바탕'요소도 나타나는지 확인해봅시다.   

5. 이제 '바탕'요소를 dropdown 위치로 옮겨보겠습니다.   
이를 위해 dropdown의 크기와 위치를 구해서, background의 크기와 위치로 지정해줍니다.   
위치 구하기 참고: <https://mommoo.tistory.com/85>   
자바스크립트로 css접근하기 : <https://ibrahimovic.tistory.com/56>   
여기서 한가지 주의할 점이 있습니다. background는 상위 태그인 nav.top 요소의 위치에 영향을 받는데 반해서, dropdown 요소는 영향을 받지 않습니다. (css 관련 내용인데 자세히 다루지는 않겠습니다)   
따라서 background의 위치는 nav.top의 위치값으로 조정해주어야합니다.   
보다 구체적으로는 nav.top의 top값만큼 background의 top값을 빼줘야합니다.   

여기까지 구현하면 handleEnter 함수는 마무리됩니다.   

6. 마지막으로 handleLeave 함수를 구현해줍니다.
handleEnter에서 추가해주었던 클래스들을 제거해주기만 하면 됩니다.   
'trigger-enter', 'trigger-enter-active', 'open' 모두 제거해줍시다.

7. 앞에서 handleEnter를 구현할 때 'trigger-enter'와 'trigger-enter-active'를 나누었던 부분을 조금 더 살펴봅시다.   

이렇게 클래스를 2개로 나눈 이유는 조금 더 자연스러운 움직임을 구현하기 위해서입니다.   
'바탕'이 먼저 뜨고 '내용'이 나타나야 자연스러운 움직임이 됩니다.   
(반대로 '내용'이 먼저 나타나면 조금 어색합니다)   
이를 구현하기 위해 먼저 'trigger-enter'에서 display값을 바꾸어서 화면 상에 요소를 위치시켜주고,   
그 후에 'trigger-enter-active'로 투명도를 바꿔서 화면 상에 나타나도록 해줍니다.   

여기서 구현해야하는 것은, 'trigger-enter-active'가 동작하기 전에 '바탕'이 먼저 나타나야한다는 것입니다.