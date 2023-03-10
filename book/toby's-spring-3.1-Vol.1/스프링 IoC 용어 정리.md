# 스프링 IoC 용어 정리
### 빈(bean)
빈 또는 빈 오브젝트는 스프링이 IoC 방식으로 관리하는 오브젝트라는 뜻이다.
스프링이 직접 그 생성과 제어를 담당하는 오브젝트만을 빈이라고 부른다.

### 빈 팩토리(bean factory)
스프링의 IoC를 담당하는 핵심 컨테이너를 가리킨다. 빈을 등록하고, 생성하고, 조회하고 돌려주고, 
그 외에 부가적인 빈을 관리하는 기능을 담당한다. 보통은 이를 확장한 애플리케이션 컨텍스트를 사용한다.
BeanFactory라고 붙여쓰면 빈 팩토리가 구현하고 있는 가장 기본적인 인터페이스의 이름이 된다.
getBean()과 같은 메서드가 정의되어 있다.

### 애플리케이션 컨텍스트(application context)
빈 팩토리라고 부를 때는 주로 빈의 생성과 제어의 관점에서 이야기하는 것이고,
애플리케이션 컨텍스트라고 할 때는 스프링이 제공하는 애플리케이션 지원 기능을 모두 포함해서 이야기하는
것이라고 보면 된다.
```
DaoFactory 가 아닌 애플리케이션 컨텍스트를 사용했을 때 얻는 장점
- 클라이언트는 구체적인 팩토리 클래스를 알 필요가 없다.
- 애플리케이션 컨텍스트는 종합 IoC 서비스를 제공해준다. (오브젝트 후처리, 만들어지는 시점 인터셉팅 등)
- 애플리케이션 컨텍스트는 빈을 검색하는 다양한 방법을 제공한다.
```
### 설정정보/설정 메타정보(configuration metadata)
스프링의 설정정보란 애플리케이션 컨텍스트 또는 빈 팩토리가 IoC를 적용하기 위해 사용하는 메타정보를 말한다.
IoC 컨테이너에 의해 관리되는 애플리케이션 오브젝트를 구성할 때 사용된다.

### 컨테이너 또는 IoC 컨테이너
IoC 방식으로 빈을 관리한다는 의미에서 애플리케이션 컨텍스트와 빈 팩토리를 IoC 컨테이너라고도 한다.
애플리케이션 컨텍스트는 그 자체로 ApplicationContext 인터페이스를 구현한 오브젝트를 가리키기도 하는데,
애플리케이션 컨텍스트는 하나의 애플리케이션에서 보통 여러개가 만들어져 사용된다. 이를 통틀어서 스프링 컨테이너라고 부를 수 있다.



