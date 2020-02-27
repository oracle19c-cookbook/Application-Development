## 소개

![](https://github.com/oracle19c-cookbook/Application-Development/blob/master/JSON/json.png)

Oracle 데이터베이스는 JSON 데이터 모델에 기반한 Schema-less 애플리케이션 개발을 완벽하게 지원합니다. 이를 통해 통상의 NoSQL 문서 저장소가 제공하는 스키마 유연성의 특징 및 및 신속한 애플리케이션 개발 방법론을 Oracle 데이터베이스의 일체의 엔터프라이즈 급 기능들과 결합하여 사용할 수 있습니다.

- **Simple Oracle Document Access (SODA)**  
    SODA API를 이용하면 개발자는 SQL을 사용하지 않고도 Oracle DB에 저장된 JSON 문서에 대한 작업을 할 수 있습니다. SODA는 REST, Java, Node.js, Python, PL/SQL 및 OCI를 포함한 여러 언어 및 프레임워크에서 지원됩니다.

- **SQL 접근**  
    Oracle DB에 저장된 JSON은 변환 과정 없이 표준 SQL을 통해 직접 액세스할 수 있습니다. 기존의 관계형 테이블과의 조인도 당연히 가능합니다.

- **ACID 트랜잭션**  
    JSON 문서에도 기존 관계형 데이터에 적용되는 트랜잭션의 ACID property가 그대로 적용되므로, 관계형 DB를 사용할 때와 동등한 읽기 일관성과 동시 사용성을 확보할 수 있습니다. 

- **Oracle DB 플랫폼에 통합**  
    더 이상 개발 용이성과 엔터프라이즈 데이터 관리 기능 중에서 택일할 필요가 없습니다. Oracle JSON은 암호화, 접근 제어 및 감사를 통한 안전한 데이터 처리, RAC를 통한 가용성 및 확장성, Oracle Multitenant 아키텍처와의 통합을 완벽하게 제공합니다.
    
    
## Hands-On

- [LiveSQL 튜토리얼](https://livesql.oracle.com/apex/livesql/file/tutorial_EDVE861H6UF4Z20EV0RM4DK2G.html)
- [GitHub 샘플 코드](https://github.com/oracle/json-in-db) 


## 참고 자료

- [백서: Oracle 데이터베이스를 이용한 Schemaless 어플리케이션 개발](https://www.oracle.com/technetwork/database/schemaless-appdev-2603887.pdf)
- [백서: SODA를 이용한 Schemaless 어플리케이션 개발](https://www.oracle.com/technetwork/database/appdev-with-soda-2606220.pdf)
- [샘플 어플리케이션: Oracle Movie Ticketing Application (NODE.js with Soda for REST)](https://www.oracle.com/technetwork/database/oracle-moivie-ticketing-12c-node-3407483.pdf)
- [백서: Oracle DB 내의 JSON 데이터 조회](https://www.oracle.com/technetwork/database/sql-json-wp-2604702.pdf)
