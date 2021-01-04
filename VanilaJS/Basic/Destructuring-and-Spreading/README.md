## Destructuring and Spreading

### 참고할 교재
- poiemaweb ECMAScript6 4장, 6장, 11장   

poiemaweb이 너무 어려우면   
- [Destructuring](https://dataguru.kr/es6-%eb%94%94%ec%8a%a4%ed%8a%b8%eb%9f%ad%ec%b2%98%eb%a7%81destructuring/)
- [Spread & Rest 연산자](https://dataguru.kr/es6-spread-rest-%ec%97%b0%ec%82%b0%ec%9e%90/)
- [for ... of 루프](https://dataguru.kr/es6-for-of-%eb%a3%a8%ed%94%84/)


### 문제
1. destructuring을 사용해서 constants에 있는 요소들을 e, pi, gravity, humanBodyTemp, waterBoilingTemp에 할당해보세요.   

2. destructuring을 사용해서 countries에 있는 요소들을 fin, est, sw, den, nor에 할당해보세요.   

3. destructuring을 사용해서 rectangle 객체에 있는 요소들을 키(변수)에 할당해보세요.   

4. users를 순회(iterate)해서(for .. of 사용) 키에 해당하는 값들을 콘솔에 차례로 출력해보세요.   

5. users에 있는 user들 중 skill이 2개 이하인 user의 name만 콘솔에 출력해보세요. (for .. of 사용)   

6. convertArrayToObject라는 이름의 함수를 만들어보세요.   
입력으로 배열을 받아서 객체 형태로 변환된 값을 리턴해주는 함수입니다.   
students 배열을 함수에 집어넣으면 아래와 같이 동작합니다.   

```javascript
const students = [
    ['David', ['HTM', 'CSS', 'JS', 'React'], [98, 85, 90, 95]],
    ['John', ['HTM', 'CSS', 'JS', 'React'], [85, 80, 85, 80]]
]

console.log(convertArrayToObject(students))

[
    {
        name: 'David',
        skills: ['HTM','CSS','JS','React'],
        scores: [98,85,90,95]
    },
    {
        name: 'John',
        skills: ['HTM','CSS','JS','React'],
        scores: [85, 80,85,80]
    }
]
```

7. student 객체를 newStudent 객체에 복사(copy)해보세요.(spread 연산자 사용)   
원본 student 객체는 변화시키지 않습니다.   
복사하면서 newStudent 객체에는 다음과 같은 값들을 추가해주세요.   
- frontEnd 스킬셋에 level 8의 Bootstrap
- backEnd 스킬셋에 level 9의 Express
- dataBase 스킬셋에 level 8의 SQL
- dataScience 스킬셋에 SQL   

복사한 결과는 다음과 같이 나와야합니다.
```javascript
const student = {
      name: 'David',
      age: 25,
      skills: {
        frontEnd: [
          { skill: 'HTML', level: 10 },
          { skill: 'CSS', level: 8 },
          { skill: 'JS', level: 8 },
          { skill: 'React', level: 9 }
        ],
        backEnd: [
          { skill: 'Node',level: 7 },
          { skill: 'GraphQL', level: 8 },
        ],
        dataBase:[
          { skill: 'MongoDB', level: 7.5 },
        ],
        dataScience:['Python', 'R', 'D3.js']
      }
}


console.log(newStudent);
{
    name: 'David',
    age: 25,
    skills: {
      frontEnd: [
        {skill: 'HTML',level: 10},
        {skill: 'CSS',level: 8},
        {skill: 'JS',level: 8},
        {skill: 'React',level: 9},
        {skill: 'BootStrap',level: 8}
      ],
      backEnd: [
        {skill: 'Node',level: 7},
        {skill: 'GraphQL',level: 8},
        {skill: 'Express',level: 9}
      ],
      dataBase: [
        { skill: 'MongoDB',level: 7.5},
        { skill: 'SQL',level: 8}
      ],
      dataScience: ['Python','R','D3.js','SQL']
    }
}
```
