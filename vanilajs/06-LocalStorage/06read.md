# 문제-06
TODO 리스트를 관리하는 프로그램을 만들어봅니다.   

index.html 파일을 브라우저에서 열어보면, Item을 입력하는 창과 Item을 추가하는 버튼이 있습니다.   

다음의 3가지 기능이 동작하도록 구현합니다.   
1. TODO항목을 입력하고 추가버튼을 누르면, 그 아이템이 localStorage에 저장되고, 입력된 Item이 위에 뜨도록 해야합니다.   
2. 여러 항목들을 더 입력하고 추가하면 그 Item들의 리스트가 모두 뜨도록 해야합니다.(localStorage에도 모두 저장합니다)   
3. 또 각각의 Item에는 체크박스가 있어서 Item을 체크해서 완료표시를 할 수 있도록 합니다.(역시 localStorage에도 업데이트 되어야합니다)   

자바스크립트 localStorage 참고 : <https://ponyozzang.tistory.com/341>

3가지 함수를 만들어서 구현합니다.   
첫번째 함수는 addItem입니다. 폼 태그요소인 addItems에 'submit'이벤트로 바인딩합니다.   
itemsList에 아이템을 추가하고, localStorage에도 저장시키는 역할을 합니다.   

두번째 함수는 toggleDone입니다. ul 태그요소인 itemsList에 'click'이벤트로 바인딩합니다.  
itemsList에 있는 항목들 중 하나를 체크했을 때, 완료표시가 되도록 동작합니다. 역시 localStorage에도 반영되어야합니다.

세번째 함수는 populateList입니다. TODO 목록을 다시 갱신해주는 역할을 합니다. addItem과 toggleDone 내부에 넣어주어서 아이템을 추가할 때, 또는 아이템을 완료시켰을 때 populateList가 동작하도록 합니다.   

--

먼저 items 상수를 살펴봅시다. 이전에 저장된 아이템들이 있다면 모두 불러와야합니다. (localStorage.getItem('items'))   
localStorage로 가져온 아이템은 문자열 형태이기때문에 자바스크립트가 이해하는 JSON객체로 변환해주어야합니다. 이를 위해 JSON.parse를 사용합니다.   

items는 객체들로 이루어진 배열 자료형입니다.

JSON 참고 : <http://tcpschool.com/json/json_use_js>

이제 각각의 함수를 더 살펴봅시다.   
1. addItem   

input태그요소에서 입력된 값을 가져와서 item 상수에 저장합니다.   
item은 다음과 같은 객체 형식입니다.   
{   
    TODO항목,   
    done: true/false   
}   

그 후 item을 items 배열에 집어넣고, populateList로 리스트를 갱신해줍니다.   
그리고 localStorage에 'items'항목으로 items를 넣어줍니다. 여기서 items를 바로 넣으면 안되고 배열을 문자열로 다시 변환해서 넣어야합니다. (JSON.stringify 사용)   

마지막으로 input태그요소를 초기화해줍니다.(reset())   

2. toggleDone

event 객체를 인자로 받습니다.   
해당하는 input태그요소의 인덱스를 구해서 (e.target.dataset.index)
items배열의 해당요소에서 done값을 바꿔주고, localStorage에도 업데이트해줍니다.   
마지막으로 itemsList도 갱신해줍니다.(populateList)

3. populateList

todos 배열과 todosList를 인자로 받습니다.   
todos에는 items가 넘겨질 것이고, todosList에는 itemsList가 넘겨질 것입니다.   

todosList의 innerHTML에 (예를 들면) 다음과 같은 HTML 요소를 집어넣을 겁니다.
```
<li>
    <input type="checkbox" data-index=0 id="item0" 'checked' />
    <label for="item0">샤워하기</label>
</li>
<li>
    <input type="checkbox" data-index=1 id="item1"  />
    <label for="item1">독서하기</label>
</li>
<li>
    <input type="checkbox" data-index=2 id="item2" 'checked' />
    <label for="item2">산책하기</label>
</li>
```
반복되는 li태그를 처리하기 위해 배열의 map함수를 활용해보세요.   
innerHTML에 넣는 자료형은 문자열이라는 것도 꼭 숙지하세요.


