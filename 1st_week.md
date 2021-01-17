# 1st week
## 1부 - 기본개념
### 1. 데이터
---
#### 1.1 데이터
* 데이터 
    * 해석할 수 있는 의미를 가진 기호
    * 정성적(이미지, 텍스트) 또는 정량적(숫자) 변수 값의 집합
        + 정형분석(정량적) : 구조화 되어있는 데이터(ex. SQL)  
        + 비정형분석(정성적) : 구조화 되어있지 않은 데이터 (ex. 빅데이터)
#### 1.2 데이터베이스
* DataBase : 데이터를 정리해서 모아둔것
* Database model
    * 데이터를 효율적으로 관리하기 위한 모델
    * hierarchical(계층형) : 과거에 사용됨
    * network(네트워크) : 과거에 사용됨
    * relational(관계형) : 현재 사용하는 모델
* relational model
    * **relation**에 데이터를 저장.
    * relation은 2차원형태의 표로 구성된다.
    * 릴레이션은 튜플의 집합  튜플은 속성의 집합이다.

#### 1.3 데이터베이스 관리 시스템(DBMS)
* DBMS (DataBaseManagementSystem) : 데이터베이스를 관리하기 위한 응용프로그램이다.

#### 1.4 IT 시스템
* IT System : 데이터의 발생 유형과 사용 목적에 따라 구현되는 것.
* 구성
    * 운영시스템
    * EDW영역
    * BI영역

* 릴레이션
    * 운영 시스템에서 발생한 데이터는 EDW영역을 거쳐 BI영역으로 이동한다.

|영역|목적|
|:---:|:---:|
|운영시스템(Operaional System)|기업운영에 필요한 데이터를 관리|
|EDW(Enterprise Data Warehouse)|분석을 위한 데이터를 저장|
|BI(Business Intelligence)|기업의 효율적인 의사 결정을 지원|


* 운영목적에따른 시스템 관리

| 시스템 | 목적 |
|:---:|:---:|
| OLTP | 온라인 드랜젝션을 처리 |
| ODS | 운영데이터를 원본의 형태로 보관 |
| DW | 운영 데이터를 통일된 형식으로 저장 |
| DM | DW데이터를 사용 목적에 따라 요약 |
| OLAP | DW데이터를 분석 |

#### 1.5 직종과 직무


### 2. 데이터 모델링
---
* Data Modeling : 데이터를 설계하는 일련의 과정.

#### 2.1 데이터 모델
* Data Model : 현실 세계의 정보를 DB로 구축할 수 있도록 Abstraction(추상화) 한 것.<br>
ex) 카페 상품 추상화 과정

* 데이터 모델의 종류
    * Conceptual Data Model : 요구사항 분석을 분석하여 설계.
    * Logical Data Model    : 개념 데이터 모델을 논리데이터 모델로 상세화.
    * Physical Data Model   : DBMS에 따라 논리데이터모델을 물리데이터 모델로 전환.

#### 2.2 E-R 모델
* 데이터 표현 방식 : entitiy와 relationship으로 데이터를 표현.(국내에서 가장 많이 사용하는 방식)
* E-R모델의 개념
    * entity type : instance화된 엔티티의 집합
    * entity : 속성으로 구성
    * relationship : 엔티티 간의 연관, 페어링의 집합이다.
    * paring : 인스턴스간의 연관

|개념|집합|개별|
|:---:|:---:|:---:|
|어떤 것|Entitiy Type|entity<br>instance|
|어떤 것의 관계|relationship|pairing|
|어떤 것의 특징|attribute|attribute value|

|개념|집합|개별|
|:---:|:---:|:---:|
|어떤 것|Entitiy|instance|
|어떤 것의 관계|relationship|pairing|
|어떤 것의 특징|attribute|attribute value|

* ERD

#### 2.2.1 엔터티
* Entity : 개체로 인식 할 수 있는 데이터의 집합.
* 표현방식 : 사각형
* Entity 명 : 사각형 위쪽에 기술

* Primary Identifier : entity에서 instance를 고유하게 식별 할 수 있는 속성이다.
* 표현 방식 : 위쪽 사각형 안에 기술한다.
* 표현 종류
    * 단일 식별자 : 하나의 속성자로 이루어져있는 것.
    * 복합 식별자 : 둘 이상의 속성자로 이루어져있는 것.

#### 2.2.2 속성
* Attribute : 엔티티에서 관리되는 최소 단위.
* 표현 방식 : 기본 식별자가 아닌 속성은 아래쪽 사각형 안에 기술한다.

##### 2.2.2.1 Domain
* Domain : 속성 값의 범위, 물리 모델에서 데이터 타입과 제약조건으로 변환한다.
* 
#### 2.2.3 관계
* Relationship : 페어링의 집합, 엔티티간의 업무적 연관.
* 하나의 엔티티는 하나 이상의 엔티티와 관계를 가질 수 있다.
* 관계를 가진 엔티티와 또 다른 관계를 맺을 수 있다.

#### 2.2.3.1 카디널리티
* Cardinality : Pairing 개수를 나타냄. (하나의 부모 인스턴스가 몇 개의 자식 인스턴스와 페어링 될 수 있는 지를 나타낸다.)
* 

#### 2.2.3.2 옵셔널리티
* optionality : Pairing 여부. (부모 인스턴스와 자식 인스턴스의 페이링 여부.)
* 종류 
    * 필수 관계 : 페이링이 필수.
    * 선택 관계 : 페어링이 선택.
        * fully mandatory : 
        * optional : 
        * fully optional : 

#### 2.2.3.3 관계 유형
* 관계 유형 종류
    * 식별 관계 : 부모 엔티티의 기본 식별자가 자식 엔티티의 기본 식별자 속성으로 상속된 경우.
    * 비식별 관계 : 부모 엔티티의 기본 식별자가 자식엔티티의 일반속성으로 상속된 경우.

#### 2.3 정규형
* 데이터이상 현상을 제거하기 위한 관계형 모델의 설계 지침이다.
#### 2.3.1 정규화
* 1NF
    * 속성의 원자성과 관련있다.
    * 정규형의 종류
        * multiple value : 다중 값을 가진 현상.
        * repeating group : 하나의 튜플에 유사한 속성이 반복되는 현상
* 2NF
    * 부분 종속과 관련 있음.
    * partial dependency : 일반 속성이 식별자의 일부 속성에만 종속되는 것.

* 3NF
    * 이행종속과 관련이 있다.
    * transitive dependency : 일반속성이 다른 속석에 종속되는 것.
    
#### 2.3.2 반정규화
* denormalization : 일반 속성이 다른 일반속성에 종속되는 것.

#### 2.4 물리 데이터 모델
|논리 데이터 모델|물리 데이터 모델|
|:---|:---|
| Entity| Table |
| Attribute | 열 |
| Domain | 데이터 타입, NOT NULL 제약조건, CHECK 제약조건|
|primary Identifier| PK 제약조건 |
|Foreign Identifier| FK 제약조건 |

### 3. 오라클 데이터베이스
---
* 사용자 : 데이터베이스에 로그인 할 수 있는 계정.
    * SYS : Super user 계정으로 모든 권한을 가지고 있다.
    * DBA : DB관리자 계정
    * ALL : 모든 사용자
    * USER : 모든 사용자 
* 오브젝트
    * object : 논리적 데이터 구조
    * schema : 사용자에 종속된 오브젝트
    * nonschema : 사용자에 종속되지 않은 오브젝트

    |구분|오브젝트|
    |:---|:---|
    |Schema Object| 테이블, 클러스터, 인덱스, 뷰, 시퀀스, 시노님, 오브젝트 타입|
    |non-schema Object|사용자, 롤, 디렉터리|

* 세그먼트
    * segment : 저장공간이 필요한 object이다.

    |구분|오브젝트|
    |:---|:---|
    |segment object | 테이블, 클러스타, 인덱스 |
    |non-segment object| 뷰, 시퀀스, 시노님, 오브젝트 타입, 사용자, 롤, 디렉터리 |

* 데이터 무결성
    * Data Integrity : 데이터의 정확성과 일관성이 유지되고 있는 상태를 의미함.
    * 무결성 종류 
    
        |무결성|설명|
        |:---|:---|:---|
        |개체 무결성|엔티티의 인스턴스가 속성이나 속성의 조합으로 식별되어야 함.|
        |범위 무결성|속성값이 지정한 범위에 유효해야 함.|
        |사용자 정의 무결성|개체 무결성, 참조 무결성, 범위무결성에 속하지 않는 무결성.|

* 정적 데이터 딕셔너리 뷰
* 동적 성능 뷰
* 구조
    * 프로세스 구조
        * 백그라운드 프로세스 <br> 생성시기 : 인스턴스가 시작 될 때
        * 서버 프로세스 <br> 생성시기 : 사용자가 데이터베이스 서버에 접속 할 때.

    * 메모리 구조
        * SGA : 백그라운드 프로세스와 서버 프로세스의 공유 메모리 영역. 
        <br> 메모리 할당 : 인스턴스가 시작 될 때 
        <br> 메모리 해제 : 인스턴스가 종료 될때.
        * PGA : 서버 프로세스의 독점 메모리 영역.
        <br> 메모리 할당 : 서버 프로세스 생성 될때
        <br> 메모리 해제 : 서버 프로세스 종료 될때
    
### 4. SQL
---
* 종류

|종류|구문|
|:---|:---|
|SELECT|SELECT|
|DML|INSERT, UPDATE, DELETE, MERGE|
|TCS|COMMIT, ROLLBACK, SAVEPOINT, SET TRANSACTION|
|DDL|CREATE, ALTER, DROP, TRUNCATE, COMMENT|
|DCL|GRANT, REVOEK|
|SCS|ALTER SESSION, SET ROLE|