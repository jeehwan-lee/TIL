# useFocusEffect

- 화면이 포커스되었을 경우 발생하는 hook
- 화면은 stack 구조로 쌓이기 때문에 맨 아래 쌓인 화면은 useEffect만으로는 화면이 랜더링될때의 동작을 할 수 없다.
  때문에 useFocusEffect hook을 통해 화면이 focus 되었을때 동작을 넣을 수 있다.
  ```
    useFocusEffect(() => {
    console.log("focus");
    return () => console.log("cleanup Fcus");
    });
  ```
- useFocusEffect만 사용할 경우 state가 변할때마다 useFocusEffect 안의 함수가 실행되기 때문에
  다음과 같이 useCallback과 함께 사용
  ```
    useFocusEffect(
      useCallback(() => {
        console.log("focus");
        return () => console.log("cleanup Focus");
      }, [])
    );
  ```
