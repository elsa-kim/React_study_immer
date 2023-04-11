## immer 사용법

- 예시코드

```
import produce from 'immer';
const nextState = produce(originalState, draft => {
  // 바꾸고 싶은 값 바꾸기
  draft.somewhere.deep.inside = 5;
})
```

    - produce 함수는 두 가지 파라미터 받음 : 첫 번째 파라미터는 수정하고 싶은 상태, 두 번째 파라미터는 상태를 어떻게 업데이트할지 정의하는 함수
    - 두 번째 파라미터로 전달되는 함수 내부에서 원하는 값 변경하면 produce 함수가 불변성 유지해주며 새로운 상태 생성

- immer 사용해 컴포넌트 상태 작성할 때는 객체 안에 있는 값 직접 수정하거나, 배열에 직접적 변화 일으키는 push, splice 등 함수 써도 무방

- produce 함수 호출 시 첫 번째 파라미터가 함수 형태면 업데이트 함수 반환 -> useState 함수형 업데이트 함께 활용하면 코드 더욱 깔끔하게 만들 수 있음
