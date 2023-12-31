# 클린 코드 프론트엔드 | 프리온보딩 FE 챌린지 11월 (2023)

>https://www.wanted.co.kr/events/pre_challenge_fe_15
>
>과제를 제출하고 싶다면 결과물을 Gist Comment에 남겨주세요 (Link로 대체 가능)

## 챌린지 과제

### Q1. 내가 생각하는 클린 코드란?

1. 가독성이 좋은 코드
2. 중복되지 않은 코드
3. 변수명이나 함수명이 적절하게 쓰인 코드

이 외에도 많은 부분이 있겠지만, 협업할 때 정해놓은 규칙에 맞게 작성하는 코드가 클린 코드라고 생각합니다.

### Q2. 내가 생각하는 (프론트엔드에서의) 클린 코드란?

1. 변수명, 함수명을 이해하기 쉽게 명확히 작성한 코드
2. singleQuote, DoubleQuote의 통일성을 지킨 코드
3. 중복된 함수를 분리해서 사용할 수 있는 코드
4. 들여쓰기가 잘 된 코드

### Q3. 내가 클린코드보다 중요하게 생각하는 것은?

클린코드보다 우선시 되야할 것은, "정상적으로 작동되는 코드"라고 생각합니다.

클린코드가 아니라 보기 힘든 코드라도, 추후에 코드를 리팩토링하며 클린코드 규칙을 적용해 나가며
더 나은 코드로 바꿀 수 있다고 생각합니다.

하지만, 작동되지 않는 코드라면 코드의 로직부터 다시 손봐야하기 때문입니다.


### Q4. 다음 중 선호하는 방식과 그 이유는?

##### 1.
`Tab` vs `Space`

> 현재는 Tab과 Space의 정확한 차이가 인지가 되지 않은 상태이지만, 저의 경우에는 주로 Tab을 선호합니다.
> 왜냐하면 space 방식은 들여쓰기가 깊어졌을 때 스페이스로 공백을 표현해야 하는 부분에서 불필요한 시간소요가 들 것 같다는 생각이 들었습니다.

##### 2.
`세미콜론 O` vs `세미콜론 X`

> '모던 JavaScript Deep Dive' 책을 읽었을 때, 세미콜론을 쓰지 않아도 문제되는 부분은 없다.
> 하지만, 'ESLint같은 정적 분석 도구에서도 세미콜론 사용을 기본으로 설정 하고 있고, TC39(ECMAScript 기술 위원회)도 세미콜론 사용을 권장하는 분위기 이다' 라고 표현된 부분을 보았습니다.<br/>
> 공식적으로 선호하는 방식을 따르는 것이 클린코드라고 생각하기 때문에 **세미콜론**을 통해서 문장의 끝을 표현해주는 것이 좋다고 생각합니다.

##### 3.
`count++;` vs `count += 1;` vs `count = count + 1;`

> 보통 일반적인 프로그래머라면 모든 코드를 전부 이해하고 있을 것으로 생각됩니다.<br/>
> 따라서 가장 줄여서 깔끔하게 표현할 수 있는 방법인  `count++`를 사용하는 것이 좋다고 생각합니다.

##### 4.
`if (isLogin) {}` vs `if (isLogin === true) {}`

> 자바스크립트에 대한 기초적인 이해도를 가진 사람이라면 암묵적 형변환을 이해할 것이고, 이 부분을 인지하고 있다면<br/>
> `if (isLogin) {}`을 사용하는 것이 좋다고 생각합니다.

##### 5.
`isLogin && <HelloWanted />` vs `isLogin ? <HelloWanted /> : <></>` vs `isLogin ? <HelloWanted /> : null` vs `isLogin ? <HelloWanted /> : undfined`

> 저는 기본적으로 `isLogin ? <HelloWanted /> : null`을 사용해 왔습니다.<br/>
> 하지만 null이 생략되었지만 누구나 이해할 수 있는 표현인 `isLogin && <HelloWanted />`의 표현이 더 좋다고 생각됩니다.
