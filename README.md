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
* https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#appendix-dependency-versions

### Maven 사용시
- sping-boot-starter-parent 프로젝트를 부모 프로젝트로 상속한다.
```xml
<parent>
  <groupId>org.springframework.boot</groupId>
  <artifactId>spring-boot-starter-parent</artifactId>
  <version>2.0.6.RELEASE</version>
</parent>
```
- 자바 컴파일러 준수 레벨은 디폴트값은 1.8이다.


## 자동 구성
- Spring Boot 는 설정을 변경하지 않으면 미리 정해진 디폴트 설정에 따라 동작한다.
  - 자동 구성 기능이 디폴트 동작을 설정한 것이다.
  - 예를 들어 의존관계에 HSQLDB 라이브러리를 추가한 상태에서 데이터베이스에 대한 접속 설정을 정의하지 않는다면, 내장형 인메모리 데이터베이스를 데이터 소스로 사용하도록 자동으로 설정된다.
  - 자동 구성을 사용하려면 @EnableAutoConfiguration 또는 @SpringBootApplication 애너테이션을 부여한다.
  - 자동 구성은 개발자가 직접 명시한 구성을 덮어 쓰지는 않는다.
  - 현재 어떤 자동 구성이 적용되었는지 알고 싶다면 인수에 --debug를 지정해 애플리케이션을 실행하면 자동 구성 보고서가 콘솔에 출력된다.


