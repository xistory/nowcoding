# 문제-04
배열에 있는 고차함수들을 활용하며 연습해보자.

index.html을 에디터로 열어보면 script태그에 4개의 배열이 있는 것을 확인할 수 있다. (inventors, data, people, comments)   

이 4개의 배열을 사용해서 다음 문제들을 해결해보자.   

1) inventors에서 1500년대에 태어난 인물들만 뽑아보자.(Array.prototype.filter)
2) inventors에서 first와 last name로만 뽑아서 다시 나열해보자. (Array.prototype.map)
3) inventors에 있는 인물들을 태어난 연도를 기준으로 다시 나열해보자. (가장 오래된 순서로) (Array.prototype.sort)
4) inventors에 있는 인물들이 생존한 기간은 총 몇 년인가? (Array.prototype.reduce)
5) inventors에 있는 인물들을 생존한 기간을 기준으로 다시 나열해보자. (가장 오래된 순서로) (Array.prototype.reduce)
6) data배열에 있는 각각의 요소가 몇번 반복적으로 나타나는지 구해서, 객체의 형태로 정리해서 반환해보자 (Array.prototype.reduce)   
다음과 같은 형태로 반환되어야한다.   
{ bike: 2, car: 5, pogostick: 1, ….. }
7) people배열에 있는 사람들 중 19살인 사람이 최소 한 명 이상 있는지 확인해보자. (Array.prototype.some)
8) people배열에 있는 사람들이 모두 19살인지 확인해보자. (Array.prototype.every)
9) comments배열에 있는 요소 중 id가 823423인 요소를 꺼내보자. (Array.prototype.find)
10) comments배열에 있는 요소 중 id가 823423인 요소의 인덱스를 꺼내보자. (Array.prototype.findIndex)


# 필요한 문법
<https://poiemaweb.com/>   
JavaScript
- 29 배열 고차 함수

ECMAScript
- 3 화살표 함수