# CSS 선택자

## 요소선택자
태그의 이름을 적어서 사용하는 선택자입니다.\
다음과 같이 사용합니다.
```
// 코드 1-1
h1{
    style: style;
}
```

## Id 선택자
`id` 속성을 가진 요소를 선택하는 선택자입니다.\
`id` 속성은 `id` 이름 앞에 '#'을 붙여 나타냅니다.\
다음과 같이 사용합니다.
```
// 코드 1-2
#xyz{
    style: style;
}
```
## Class 선택자
`class` 속성을 가진 요소를 선택하는 선택자입니다.\
`class` 속성은 `class` 이름 앞에 '.'을 붙여 나타냅니다.\
다음과 같이 사용합니다.
```
// 코드 1-3
.xyz{
    style: style;
}
```
## 중첩 사용
예를 들어 `xyz` 클래스 속성을 갖고 있는 `div` 태그에만 스타일을 주고 싶다고 가정해봅시다.\
그럴 때에는 선택자를 중첩하여 사용해야 합니다.
```
// 코드 1-4
div.xyz{
    style: style;
}
```
```
// 코드 1-4.2
.com.xyz.abc{
    style: style;
}
```
## 선택자 묶음

```
// 코드 1-5
div{
    style: style;
}

h1{
    style: style;
}
p{
    style: style;
}
```
```
// 코드 1-6
div, h1, p{
    stlye: style;
}
```

이와 같이 똑같은 스타일을 여러 요소에 적용시켜야 할 때가 있습니다.\
`코드 1-5` 와 같이 쓰게되면 똑같은 코드를 반복하게 됩니다.\
그러나 `코드 1-6` 과 같이 ','를 이용하여 작성하면 반복되는 코드를 줄일 수 있습니다.

## 자손 선택자
```
// 코드 1-7.1 
<div class="my-box">
    <div class="title">
        Hello World
    </div>
</div>
```
```
// 코드 1-7.2
.my-box > .title{
    style: style;
}
```
`코드 1-7.2` 는 `코드 1-7.1`을 꾸미는 CSS입니다.
`>`을 이용하면 자신의 직계 자손을 선택하여 꾸밀 수 있습니다.

## 후손 선택자
```
// 코드 1-8.1
<div class="my-box">
    <div class="info">
        <span class="name">신재헌</span>
        <span class="gender">남성</span>
    </div>
</div>
```
```
// 코드 1-8.2
.my-box .gender{
    style: style;
}
```
자손 선택자와는 다르게 `>`가 아닌 띄어쓰기로 표현합니다.\
자손 선택자는 자신의 직계 자손만 선택하는 반면 후손 선택자는 자신의 모든 자식을 선택할 수 있다는 점이 다릅니다.

간단한 웹사이트 제작을 위하여 알아야하는 선택자 지식은 이 정도 입니다.\
선택자에 대해서 더 많은 정보를 원하신다면 
`https://code.tutsplus.com/ko/tutorials/the-30-css-selectors-you-must-memorize--net-16048`
위 사이트에서 정보를 얻을 수 있습니다.
