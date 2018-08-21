---
layout: splash
title: "작성중 - 리터럴(literal) 이란?"
date: 2018-08-20 20:41:00
categories: 
  - Javascript
tags:
  - Javascript
  - object
  - primitive
  - literal
---

# 들어가며

`Javascript Cookbook` 책을 보고 공부하면서 정리한 글입니다.

# 리터럴(literal)

~~~js
'이것은 문자열입니다.'
1.45
true
~~~

문자열(String), 숫자(Number), 불리언(Boolean) 과 같은 **특정한 형식의 값**을 나타냅니다. 쉽게 말해서 **데이터를 표현하는 방식**이라고 할 수 있습니다. 다음 소스를 봅시다.

~~~js
let strVariable = 'hello' // 'hello'는 문자열 리터럴
let numVariable = 100 // 100은 숫자 리터럴
~~~

`리터럴` 은 데이터를 표현하는 방식이라고 했습니다. 'hello'가 무엇인지 설명할 때, `strVariable` 의 값이라고 설명할 수 있겠지만, 이것은 변수의 값이 무엇인지를 설명한 것이지 'hello'가 무엇인지 설명한 것이 아닙니다. 'hello'는 `문자열 리터럴` 이라고 표현해야 정확히 설명했다고 할 수 있습니다.

~~~js
let obj = new Object()

let obj2 = {}
~~~

`obj`, `obj2` 변수를 `Object` 객체로 선언했습니다. `obj2` 처럼 선언한 표현방식이 리터럴 표현방식입니다.  

<!-- 
참고 사이트
- http://asfirstalways.tistory.com/21 
- http://blog.kazikai.net/?p=45
-->