---
layout: splash
title: 'React - Props 와 state'
date: 2018-08-20 20:41:00
categories:
  - React
tags:
  - React
  - props
  - state
---

# Props

- **부모 컴포넌트**

```js
class App extends Component {
  render() {
    return (
      <div className="App">
        <MyName name="리엑트" />
      </div>
    )
  }
}
```

- **자식 컴포넌트**

```js
class MyName extends Component {
  render() {
    return <div>나의 이름은 {this.props.name} 입니다.</div>
  }
}
```

1. `React`의 데이터 흐름은 단방향이다. 부모에서 자식으로
2. 단방향이기 때문에 자식 컴포넌트는 상위 컴포넌트에 대해 거의 알 수 없다.
3. `props`는 부모 컴포넌트로부터 받는 **불변성 데이터**이다.

- **부모 컴포넌트**

```js
class App extends Component {
  render() {
    return (
      <div className="App">
        <MyName />
      </div>
    )
  }
}
```

- **자식 컴포넌트**

```js
class MyName extends Component {
  static defaultProps = {
    name: '기본이름'
  }

  render() {
    return <div>나의 이름은 {this.props.name} 입니다.</div>
  }
}
```

4. `props`의 기본값을 설정할 수 있다.
5. 부모 컴포넌트로부터 `props`를 받지 못한 경우, 기본값 `defaultProps` 의 `props`가 사용된다.

# State

```js
state = {
  number: 0,
  number2: 0
}

handleIncrease = () => {
  const { number, number2 } = this.state

  this.setState({
    number: number + 1,
    number2: number2 + 2
  })
}
```

1. `State`는 컴포넌트 안에서 변경이 가능한 데이터
2. `State`는 `render`를 통한 지속적인 동기화가 필요한 경우 데이터를 표현하기 좋다.
3. 데이터 갱신은 반드시 `setState()` 비동기 함수를 통해서 해야한다.
4. 리엑트에서는 `setState` 함수가 호출되면 컴포넌트가 리렌더링 되도록 설계되어있다.

- 참고

1. <https://velopert.com/3629>
2. <http://webframeworks.kr/tutorials/react/react-dataflow/>
