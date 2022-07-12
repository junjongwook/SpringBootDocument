# SpringBootDocument
Spring Boot 관련한 문구들 모음

### Spring Boot 특징
- 스타터 : 의존관계(dependency)를 간단하게 정의하는 모듈이다.
- 빌드 도구 : 버전 해결 등 개발을 효율화하는 플러그인이다.
- 구성 클래스 : XML이 아닌 애터테이션과 자바로 설정을 작성한다.
- 자동 구성 : 디폴트 구성이 적용되며 필요한 부분만 설정하면 된다.
- 메인 애플리케이션 클래스 : 자바 명령으로 내장된 톰캣(?)을 실행한다.
- 설정 파일 : 속성을 외부 파일에 정의할 수 있으며 동작 사양을 쉽게 변경할 수 있다.

### 참고 URL
- 스프링 부트 레퍼런스 가이드
  https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#using.build-systems.starters

### 자주 사용하는 스타터
- spring-boot-starter-web
  스프링 MVC, 톰캣이 의존관계에 추가된다.
- spring-boot-starter-jdbc
  스프링 JDBC, 톰캣 JDBC 커넥션풀(Tomcat JDBC Connection Pool)이 의존관계에 추가된다.
  
* spring-boot 는 공식 아티팩트로 예약되어 있어서 신규 명칭 작성 시에 붙이지 않는다.
