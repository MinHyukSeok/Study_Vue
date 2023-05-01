# Template Syntax
- 렌더링 된 DOM을 기본 Vue instance의 data에 선언적으로 바인딩

## Text Interpolation
- 가장 기본적인 바인딩(연결)방법
- 중괄호 2개로 표기
- DTL과 동일한 형태로 작성
- Text interpolation 방법은 모두 일반 텍스트로 표현


# Directives
- v-접두사가 있는 특수 속성에는 값을 할당 할 수 있음
  - 값에는 JS 표현식을 작성할 수 있음
## 기본 구성
- ':' 을 통해 전달인자를 받을 수 있음 

## v-show
- 표현식에 작성된 값에 따라 element를 보여 줄 것인지 결정
  - boolean 값이 변경 될 때 마다 반응

# Vue advanced
## computed
- Vue instance가 가진 options 중 하나

## methods
- 호출 될 때마다 함수를 실행
- 같은 결과여도 매번 새롭게 계산

## computed
- 함수의 종속 대상의 변화에 따라 계산 여부가 결정됨
- 종속 대상이 변하지 않으면 항상 저장된 값을 반환