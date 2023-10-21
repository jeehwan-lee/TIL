# TextInput 컴포넌트

TextInput 컴포넌트의 Props는 다음과 같습니다.

## 1. KeyboardType

TextInput 컴포넌트를 클릭해 Focus 되었을때 띄울 키보드의 종류를 정합니다.

- ascii-capable
- decimal-pad
- default
- email-address
- name-phone-pad
- number-pad
- numbers-and-punctuation
- numeric
- phone-pad
- twitter
- url
- visible-password
- web-search

## 2. returnKeyType

키보드의 완료 버튼을 returnKeyType props를 통해 변경할 수 있습니다.

- done
- next
- send

## 3. secureTextEntry

웹에서 type="password" 와 같은 기능으로 secureTextEntry={true} 를 통해
입력값을 보이지 않도록 할 수 있습니다.

## 4. keyboardAppearance

키보드의 색상을 변경하는 props로 iOS에서만 적용이 됩니다.

- default : 기기의 설정에 따라 색이 결정됩니다.

- light : 밝은색 키보드가 나타납니다.

- dark : 어두운색 키보드가 나타납니다.

## 5. onChangeText

onChange와 동일하게 text가 변경되었을때 작동하는 이벤트입니다.
다만, onChange와 다르게 반환하는 값이 text 입니다.
