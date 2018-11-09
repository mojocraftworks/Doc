# Component

> 컴포넌트의 이벤트를 관리할 수 있게 하는 클래스

## Members

### VERSION `static` `String`

버전정보 문자열

## Methods

### hasOn(eventName)

컴포넌트에 이벤트가 등록됐는지 확인한다

- parameter
  - eventName
    - String
    - 등록 여부를 확인할 이벤트의 이름
- return
  - Boolean
  - 이벤트 등록 여부

### off(eventName, handlerToDetach)

컴포넌트에 등록된 이벤트를 해제한다

- parameter
  - eventName
    - String
    - 해제할 이벤트의 이름
  - handlerToDetach
    - Function
    - 해제할 이벤트의 핸들러 함수
- return
  - Component
  - 컴포넌트 자신의 인스턴스

### on(eventName, handlerToAttach)

컴포넌트에 이벤트를 등록한다

- parameter
  - eventName
    - String
    - 등록할 이벤트의 이름
  - handlerToAttach
    - Function
    - 등록할 이벤트의 핸들러 함수
- return
  - Component
  - 컴포넌트 자신의 인스턴스

### once(eventName, handlerToAttach)

이벤트가 한번만 실행된다

- parameter
  - eventName
    - String
    - 등록할 이벤트의 이름
  - handlerToAttach
    - Function
    - 등록할 이벤트의 핸들러 함수
- return
  - Component
  - 컴포넌트 자신의 인스턴스

### trigger(eventName, customEvent)

커스텀 이벤트를 발생시킨다

- parameter
  - eventName
    - String
    - 발생할 커스텀 이벤트의 이름
  - customEvent
    - Object
    - 커스텀 이벤트가 발생할 때 전달할 데이터
- return
  - Boolean
  - 이벤트 발생 여부
    - 커스텀 이벤트 핸들러에서 stop() 메서드를 호출하면 false 를 반환하고 이벤트 발생을 중단한다