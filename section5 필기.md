- 함수 안에 console.log 넣어두고 진짜 필요할 때만 실행되는게 맞는지 검토해봐야 함.
- useMemo는 리턴 값을 기억. useCallback은 함수 자체를 기억.
  - useCallback안에서 state 쓸 때 deps에도 넣어주는 것 주의
  - hooks는 선언 순서도 중요하니까 잘 살펴보기
  - 자식 컴포넌트로 함수 넘길 때는 useCallback 해줘야 함.
  - hooks는 조건문 안에 넣지 말고, 항상 최상위에 순서대로 선언해줘야 함.
