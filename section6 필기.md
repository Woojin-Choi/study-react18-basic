- useReducer

  - 리액트에서 redux랑 비슷한 효과를 볼 수 있음.
  - dispatch를 통해 어떤 액션인지 정하고, 액션을 분리해서 실제로 처리해주는게 reducer임.

    ```js
    const SET_WINNER = 'SET_WINNER' // 대문자로 하는게 일반적인 규칙.

    const reducer = (state, action) => {
        switch (action.type){
            case SET_WINNER':
                // state.winner = action.winner 이렇게 하면 안됨
                return {
                    ...state,
                    winner: action.winner
                }
            ...
        }
    }

    const [state, dispatch] = useReducer(reducer, initialState);

    const onClickTable = () => {
        dispatch({type: SET_WINNER, winner: '0'}); // action
    }

    ```

  - useReducer에서는 불변성을 지키기 위해 가독성이 나쁨. immer 라이브러리 사용하면 되긴 함.

- 기존 js로는 데이터 변경 + 화면 그리기 까지 신경써줘야 했는데
  - 리액트는 화면에 알아서 표시해줘서 편함.
- 결국 reducer도 넘겨줘야 해서 context 쓴다고.

### 추가 공부

- immutable
- 얕은 복사 깊은 복사
  - spread문
  - JSON.stringify()
