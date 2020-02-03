# TODO list console app version 3

## Summary
![todo-list-console3](https://user-images.githubusercontent.com/35681772/73604203-0eadb280-45d0-11ea-94e2-cf901df5c92a.gif)

공부하기 위한 TODO list 콘솔 어플리케이션.
기존에 개발했던 어플리케이션을 피드백을 바탕으로 개선하여 3번째 다시 개발함.

## 기술 스택
 * Java(version: '12.0.1')
 * JUnit(version: '4.12')
 * Jupiter(version: '5.5.2')
 
## 기능 목록
 * 기본 기능
   * 메뉴를 표시한다.
   * 명령어를 입력받는다.
 
 * 할 일 생성
   * id를 생성한다.
   * 할 일을 생성한다.
   * 할 일을 생성할 때 의존성이 있는 경우 설정할 수 있다.
   * 할 일을 생성할 때 의존성이 있는 경우 존재하지 않는 할 일 id의 의존은 예외를 던진다.
   * 할 일을 생성할 때 자기 자신을 의존하도록 의존성을 설정하는 경우 메세지를 출력하며 해당 의존에 대해서만 무시된다.
   * 할 일은 id, 내용, 의존성이 있어야 생성된다.
   * 할 일을 생성할 때 내용이 공백이면 예외를 던진다.
   * 할 일은 다른 할 일과 의존성을 가질 수 있다.
   * 할 일은 생성과 동시에 생성 시간이 자동으로 할당된다.
   * 할 일은 id, 내용, 의존성, 작성 시간, 최종 수정 시간, 완료 시간에 대한 정보를 제공한다.

 * 할 일 추가
   * 새로운 할 일을 리스트에 추가한다.
   
 * 할 일 조회
   * 할 일을 id로 조회한다.
   * 리스트에 존재하지 않는 할 일 id에 대한 조회는 예외를 던진다.
   
 * 할 일 수정
   * 할 일의 내용을 수정할 수 있다.
   * 할 일은 다른 할 일과 의존성을 가지도록 수정할 수 있다.
   * 할 일을 수정할 때 존재하지 않는 할 일의 id에 대한 수정은 예외를 던진다.
   * 할 일을 수정할 때 의존성은 수정시 입력된 값으로 새롭게 갱신된다.
   * 할 일을 수정할 때 의존성이 있는 경우 존재하지 않는 할 일 id의 의존은 예외를 던진다.
   * 할 일을 수정할 때 자기 자신을 의존하도록 의존성을 설정하는 경우 메세지를 출력하며 해당 의존에 대해서만 무시된다.
   * 할 일이 수정되면 수정 시간이 자동으로 갱신된다.
      
 * 할 일 삭제
   * 삭제할 할 일의 id를 입력 받아 할 일을 삭제한다.
   * 할 일을 삭제할 때 존재하지 않는 할 일의 id에 대한 삭제는 예외를 던진다.
   * 다른 할 일이 의존하는 할 일을 삭제하려는 경우 예외를 던진다.
   * 할 일을 객체를 받아와 일치하는 객체를 삭제한다.
   * 할 일을 삭제할 때 리스트에 존재하지 않는 할 일 객체에 대한 삭제는 예외를 던진다. 
 
 * 할 일 완료
   * 할 일을 완료하면 완료 시간이 자동으로 할당된다.
   * 완료할 할 일의 id를 입력 받아 할 일을 완료한다.
   * 할 일을 완료할 때 존재하지 않는 할 일의 id에 대한 완료는 예외를 던진다.   
   * 다른 할 일(자식)이 의존하는 할 일(부모)을 완료하려는 경우 다른 모든 할 일(자식)이 완료되었을 때 완료할 수 있다.
   * 다른 할 일(자식)이 의존하는 할 일(부모)을 완료하려는 경우 다른 모든 할 일(자식)이 완료되지 않았을 때 예외를 던진다.
 
 * 예외
   * 허용되지 않는 값이 입력된 경우 이유를 출력하고 메뉴를 다시 출력한다.