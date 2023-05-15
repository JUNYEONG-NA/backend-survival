# DB ( Database )

### 학습 키워드 
* Database란
* DBMS(Database Management System)
* RDBMS(Relational Database Management System)
* 데이터베이스 언어
  * DDL
  * DML
  * DCL
* SQL
* 데이터 모델(Data Model)
  * 관계형데이터모델(ER Model)
* 튜플


## Database 

> Database란?         
> *Organized collection of data stored and accessed*       
> 구조화된 정보 or 데이터의 조직화된 모음       
> 이 말은 즉, 체계적으로 저장하고 접근한다는 뜻임.

## DBMS

최종 사용자, 응용프로그램이 데이터 베이스에서 데이터를 쉽게 찾을 수 있어야 하고 효율적인 조작, 접근 권한과 보안 문제를 다룰 수 있어야 하기 때문에 사용하는 것이 **DBMS**      

현재 현업에서 주로 쓰이는 MySQL, MariaDB, PostgreSQL, MSSQL, Oracle 등은 모두 RDBMS(Realational Database Management System)에 속한다.
> DB라고 부르는 것은 DBMS, 그중에서도 **RDBMS**를 의미하는 것이 일반적이다.

#### 데이터베이스 언어
> DBMS는 데이터베이스 언어를 제공한다.
> * DDL(Database Definition Language) - Schema (정의어)
>   * Create(생성), Alter(변경), Drop(삭제), Rename(이름변경), Truncate
>       : 테이블과 같은 데이터 구조를 정의하는데 사용되는 명령어      
> * DML(Database Manipulation Language) - Query, Command (조작어)
>   * Select : DB에 있는 데이터를 조회
>   * INSERT,UPDATE,DELETE : DB에 데이터를 삽입하거나 수정, 삭제
> * DCL(Database Control Language) - (제어어)
>
> 이들은 모두 SQL로 표현됨

## Data Model

데이터 모델은 크게 3가지 구분함

1. Conceptual Data Model
2. Logical Data Model
3. Physical Data Model

### Relational Model
> 가장 인기있는 논리적 데이터 모델,     
> 다른 논리적 데이터 모델로는 Hierachical, Network, Object-based Model이 있다.      

Entity-Relationship Model과 Relation Model은 다르다.     
ERM은 Relationship은 엔티티 사이의 관계를 의미하고, RM에서 Relation은 "Tuple의 집합(거칠게 테이블)"을 의미한다.

관계형 모델에서 쓰이는 3개념 
  1. Relation
  2. Tuple
  3. Attribute
