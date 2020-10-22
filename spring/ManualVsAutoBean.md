# 자동 빈 등록 vs 수동 빈 등록

> Q. 어떤 상황에 자동 빈을 사용하고 어떤 상황에 수동 빈을 사용해야 할까?

애플리케이션은 크게 업무 로직과 기술 지원 로직으로 나눌 수 있습니다. 
- **업무 로직 빈**: 웹을 지원하는 컨트롤러,  핵심 비즈니스 로직이 있는 서비스,  데이터 계층의 로직을 처리하는 리포지토리등이 모두 업무 로직입니다.  
보통 비즈니스 요구사항을 개발할 때 추가되거나 변경된다.
  
- **기술 지원 빈**: 기술적인 문제나 공통 관심사(AOP)를 처리할 때 주로 사용되는 빈입니다.  
데이터베이스 연결이나, 공통 로그 처리 처럼 업무 로직을 지원하기 위한 하부 기술이나 공통 기술들을 의미하며      
보통 애플리케이션 전반에 걸쳐서 광범위하게 영향을 미치는 특지을 가지고 있습니다.  
업무 로직은 문제가 발생했을 때 어디가 문제인지 명확하게 잘 들어나지만,  
기술 지원 로직은 적용이 잘 되고 있는지 아닌지 조차 파악하기 어려운 경우가 많기 때문에
 **가급적 수동 빈** 등록을 사용해서 명확하게 들어내는 것이 좋습니다.   


**애플리케이션에 광범위하게 영향을 미치는 기술 지원 객체다는 수동 빈으로 등록해서 설정 정보에 바로 나타나게 하는 것이 유지보수 하기 좋습니다.**

출처: [인프런 - 스프링 핵심 원리 기본편(김영한님)](https://www.inflearn.com/course/%EC%8A%A4%ED%94%84%EB%A7%81-%ED%95%B5%EC%8B%AC-%EC%9B%90%EB%A6%AC-%EA%B8%B0%EB%B3%B8%ED%8E%B8) 