# JMeter-Practice 
JMeter 연습용 코드 저장소입니다.
  
## basic01 : 기본적인 JMeter구조   
  + 사용한 Component   
    + Test Plan > Scenario
        + Thread Group > Script ( 가상유저 할당 )
            + Transaction Controller > 트랜잭션 단위 
                + Dummy Sampler > 서버 요청/응답 시뮬레이션  
                + Listener > 응답값 확인
                + Constant Timer > Fixed Interval 설정
                 
  + 사용한 플러그인
    + Dummy Sampler : 코드 검증 용 Sampler
    + Blaze Meter Step by Step Debugger : 코드 검증용 디버거
    + 3 Basic Graph : 테스트 결과 확인 
    
  + Scope와 실행 순서
    + Component 종류와 Tree Node 위치에 따라 적용 범위와 실행 순서가 정해짐 
    + 처음 JMeter 사용시 가장 어려운 부분임
    + 디버거를 이용하여 확인해 보면서 적응할 필요 있음 
    + 기본 Rule 
        + Node 위치에 상관 없이 Component 종류에 따라 정해지는 실행 순서 
            + Configuration elements 
            + Pre-Processors
            + Timers 
            + Samplers
            + Post-Processors
            + Assertions 
            + Listeners 
        + Scoping 
            + 같은 Parent 를 가지는 Component 에  모두 적용됨 
                + 예: Timer 는 부모 Transaction Controller 에 포함 되는 모든 Sampler 에 적용  

    
