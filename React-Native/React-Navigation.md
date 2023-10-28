# React-Navigation

애플리케이션에서 각 화면을 관리하고 이동하기 위한 기능을 제공하며,
스택, 탭, 드로어 내비게이터가 있습니다.

- npm install @react-navigation/native 를 통해 설치
- <NavigationContainer> 컴포넌트로 감싸서 사용

## 1. 네이티브 스택 내비게이터

- 스택 내비게이터를 사용하기 위해서는 @react-navigation/native-stack 필요
- createNativeStackNavigator 함수를 통해 내비게이터를 생성
- Navigator 태그의 initialRouteName을 통해 첫 화면을 설정할 수 있음
- props 종류
  - headerShow : 화면의 윗부분에 title을 보여줄지 여부를 설정

```
const Stack = createNativeStackNavigator()

const Authstack = () => {
    return (
        <Stack.Navigator initialRouteName="signIn">
            <Stack.Screen name="signIn" component={SignInScreen} />
        </Stack.Navigator>
    )
}
```

## 2. Screen 컴포넌트

```
const signIn = ({navigation, route}) => {
    return (
        ...
    )
}
```

- 등록된 화면 컴포넌트의 props로 navigation과 route가 전달됨
- navigation.push('signIn') 또는 navigation.navigate('signIn')을 통해 signIn 컴포넌트로 이동
- push는 화면을 새로 쌓지만 navigate는 동일한 화면은 그대로 둠
- 다만, navigation에 데이터를 전달할때 데이터가 바뀌면 화면을 새로 랜더링
- navigation.pop()을 통해 이전 화면으로 이동

## 3. useNavigation Hook

각 컴포넌트의 props로 전달되는 navigation을 다른 컴포넌트에 전달하지 않고 사용할 수 있도록 각 컴포넌트 내부에서 navigation을 사용할 수 있는 Hook

```
const navigation = useNavigation();

```
