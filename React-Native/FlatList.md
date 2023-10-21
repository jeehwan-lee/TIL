# FlatList

화면에 스크롤이 적용될때 사용되는 컴포넌트로 ScrollView와 FlatList가 있습니다.

- ScrollView는 화면에 보여줄 데이터를 한번에 모두 랜더링
- FlatList는 필요한 만큼만 랜더링

## 1. FlatList

FlatList를 사용하기 위한 필수 props는 data와 renderItem

- data : 랜더링할 데이터를 배열 형태로 전달
- renderItem : 받은 데이터를 어떤 컴포넌트의 형태로 랜더링할지 설정

```
<FlatList
    data={[item1, item2, item3, ...]}
    renderItem={({item}) => {
        return (
            ....
        )
    }}

>
```

- keyExtractor : Javascript의 index와 같은 역할로 각 컴포넌트의 인덱스를 생성
- windowSize : 한번에 랜더링할 양을 결정
  기본값은 21이며, 이전 10개의 화면과 현재 화면 1개 그리고 이후 화면 10개를 미리 랜더링
- ItemSeparatorComponent : 랜더링되는 각 Item 사이를 매꿀 컴포넌트를 생성
- ListHeaderComponent : 목록의 가장 상단에 보여줄 컴포넌트를 생성
- ListFooterComponent : 목록의 가장 하단에 보여줄 컴포넌트를 생성
