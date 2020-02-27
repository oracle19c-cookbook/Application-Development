## 소개

![](https://github.com/oracle19c-cookbook/Application-Development/blob/master/App%20continuty/App_continuity.jpg)

Application Continuity는 Oracle Real Application Clusters 및 Oracle Active Data Guard 옵션에서 사용할 수 있는 기능으로 데이터베이스 서버 단의 장애 발생 후 그 복구 과정이 이루어지는 과정에서, 장애 발생 시점에 이미 실행 중이었던 세션도 자동으로 복구해 주는 기능입니다. 사용자 및 어플리케이션 입장에서는 장애가 약간의 지연된 실행으로 나타날 뿐 서비스의 중단을 경험하지 않습니다.

Application Continuity는 서버 장애와 같은 계획되지 않은 다운타임은 물론이고 유지 보수 작업과 같은 계획된 다운 타임 모두에 적용되어 고가용성 경험을 극대화시킵니다.

- Application Continuity 기능은 데이터베이스 서버 단과 클라이언트 단 양쪽에서 적절한 설정을 필요로 합니다.
    - 서버 단
        - Database 서비스 정의 및 활성화
        - Autonomous DB의 경우 환경 구성이 이미 된 상태
    - 클라이언트 단
        - TNS 엔트리, Connection string, 그리고 어플리케이션 property 설정
        - 지원하는 어플리케이션은 다음과 같습니다.
            - Oracle JDBC Universal Connection Pool for both JDBC thin and OCI interfaces 
            - ODP.NET Connection Pool for Unmanaged and Managed Providers
            - Oracle clients including SQL*PLUS
            - PHP
- Application Continuity 기능의 이면에서 데이터베이스 코어 단의 Transaction Guard 메카니즘이 동작합니다.  
    Transaction Guard는 오라클이 제공하는 트랜잭션 관리 프로토콜입니다. Transaction Guard는 각 트랜잭션에 unique한 transaction identifier (LTXID)를 부여하고 관리함으로써 서버 단의 outage 발생 시에 실행 중이던 트랜택션의 정확한 commit 결과를 확보하여 클라이언트에 반환하고, 나아가 동일한 트랜잭션이 오직 한번만 적용되는 것을 보장합니다. 이는 자체 개발 또는 외부 솔루션을 이용하는 것보다 오버 헤드가 적고 성능이 훨씬 뛰어나므로 클라우드 및 인터넷 수준의 정확성과 확장성을 보장합니다.
    
## Hands-On

- [Oracle Database와 Java 성능, 확장성, 고 가용성, 보안](https://www.oracle.com/webfolder/technetwork/tutorials/obe/db/12c/r1/appdev/Java_JDBC_12c_HOL_2013_latest/Java_JDBC_12c.html)
    - *Transaction Guard for Java*, *Application Continuity for Java* 편 참조

## 참고 자료

- [Application Continuity Standalone 데모](https://www.oracle.com/technetwork/database/options/clustering/applicationcontinuity/learnmore/appconndemo-1967318.zip)
- [Application Continuity WebLogic Server 데모](https://www.oracle.com/technetwork/database/options/clustering/applicationcontinuity/learnmore/ac-wls-integration-2045376.mp4)
- [백서: Oracle 데이터베이스와 Application Continuity](https://www.oracle.com/technetwork/database/options/clustering/ac-with-oracle-database-5303807.pdf)
- [백서: Continuous Availability](https://www.oracle.com/technetwork/database/options/clustering/applicationcontinuity/continuous-service-for-apps-on-atpd-5486113.pdf)
- [백서: Transparent Application Continuity를 위한 Best Practices](https://www.oracle.com/technetwork/database/options/clustering/applicationcontinuity/learnmore/ac-applicationguidelines-5440853.pdf)
