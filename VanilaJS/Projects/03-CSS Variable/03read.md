# 문제-03
브라우저에서 index.html을 열면 아래에 이미지가 하나 나오고 그 위로 범위지정이 가능한 입력기가 3개 나옵니다.   

Spacing값에 따라서 이미지의 padding이 바뀌어야하고   
Blur값에 따라서 이미지의 선명도가 바뀌어야하고(css filter 사용)   
base값에 따라서 이미지의 backgroud 색이 바뀌어야합니다.   
css filter 참고 : <http://jinny.dothome.co.kr/2019/01/16/css-filter-%EC%82%AC%EC%9A%A9%ED%95%98%EA%B8%B0/>

index.html에서 style태그를 살펴보면 img태그의 프로퍼티값이 CSS variable을 통해 정해지는 것을 볼 수 있습니다.   
CSS variable 참고 : <https://injeblog.tistory.com/81>   

자바스크립트로 input 태그들을 모두 선택한 다음, 해당하는 css 프로퍼티값을 변경시켜주는 handleUpdate함수를 만들어서 input태그들에 이벤트로 바인딩시킵니다.   

id가 spacing, blur인 input태그는 mousemove 이벤트로 바인딩하고, (범위지정 입력이기때문)   
id가 base인 input태그는 change 이벤트로 바인딩시킵니다.   

handleUpdate함수를 만들 때는 addEventListener방식에서의 this바인딩을 염두에 두어야합니다. (poiemaweb 32장 이벤트 참고)   
css 프로퍼티값의 단위는 input태그의 data-sizing 어트리뷰트값을 활용해주세요.   
자바스크립트로 CSS 제어하기 참고 : <https://ibrahimovic.tistory.com/56>

# 필요한 문법
<https://poiemaweb.com/>   
HTML
- 9 사용자와의 커뮤니케이션을 위한 폼 태그

CSS
- 4 박스 모델

JavaScript
- 

ECMAScript
- 