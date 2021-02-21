## 📝 디자인패턴 Q&A

### View의 역할은 무엇일까요?

```
페어와 MVC 패턴에 대해 논의하던 중 View 의 역할 범위에 대해 궁금한 점이 생겼는데요.

의견1: View는 M-C 에서 다룬 데이터와 비즈니스 로직을 기반으로 최종 렌더링 부분만 담당한다.
의견2: View는 사용자가 가장 처음 마주하는 부분이기 때문에 최종 렌더링 뿐만 아니라 입력 관련 로직도 처리해야 한다. (이벤트 리스너 등)
다른 분들의 생각도 들어보고 싶습니다.
```

- 같은 이유로 처음에는 이벤트 리스너와 같은 부분을 View에 넣어야 된다고 생각했는데 최종적으론 Controller에 넣는게 더 적절하다고 생각합니다.
- 재사용성 측면에서 다른 컨트롤러가 붙어도 동작이 가능하려면 뷰는 렌더링만 담당하는것이 좋습니다. 동작에 변화를 주려면 컨트롤러단만 보면 되니까 유지보수도 쉬워집니다.
- 참고자료
  - [Best place to put the event listeners (Controller or View)](<https://forum.sencha.com/forum/showthread.php?283525-Best-place-to-put-the-event-listeners-(Controller-or-View)>)
  - [[설계 용어] 응집도와 결합도](https://medium.com/@jang.wangsu/%EC%84%A4%EA%B3%84-%EC%9A%A9%EC%96%B4-%EC%9D%91%EC[…]7%91%EB%8F%84%EC%99%80-%EA%B2%B0%ED%95%A9%EB%8F%84-b5e2b7b210ff)
