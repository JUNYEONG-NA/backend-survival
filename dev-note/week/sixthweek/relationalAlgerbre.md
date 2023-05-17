# Relational Algebre

### 학습 키워드 
* 관계대수

하나 이상의 Relation으로 새로운 Relation을 만들 수 있음.

SQL에서 연산을 통해 얻는 새로운 것 또한 Relation이다.

  * 단항연산 : Select, Projection, Rename, ... 
  * 이항연산 : Cartesian, Product, Set union, Set Diffenence, ...

## Projection
원하는 Attribute를 포함하는 Pair로 Tuple을 구성.      
SQL에선 SELECT절 바로 뒤에 속성 이름을 나열하는 방시긍로 표현.      

    SELECT name, age, gender
    FROM people;

특별히 속성을 제한하고 싶지 않다면 와일드카드(*)를 사용.       

    SELECT * FROM people;

## Cartesian Product( 곱집합 )

Relation의 곱집합은 원래 의미와 다름. 관계대수에서의 곱집합은 그냥 Tuple을 합치는 것을 의미한다.

SQL에선 그냥 FROM 뒤에 관계 이름을 나열하면 된다.

    SELECT * FROM T1,T2;

