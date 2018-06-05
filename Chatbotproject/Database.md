Azure 로 데이터베이스 프로토타입 

https://portal.azure.com


SELECT

테이블에 저장된 데이터를 조회하기 위한 명령어이다.
SQL문 중에 가장 많이 쓰인다.
SELECT문에는 FROM 키워드가 반드시 따라와야 한다.


SELECT * FROM PLAYER;


# SQL 명령어

https://wikidocs.net/4088

# 테이블에 VALUE 넣기

INSERT INTO PLAYER VALUES(1)


# python에서 테이블에 value 넣기

 cursor.execute("insert into dbo.Products(ProductID,ProductName,Price) VALUES (3000, '3mm Bracket', .52)")
 
 
# Table에 있는거 모두 뽑아보기 
for 



python 연결

![sql](https://user-images.githubusercontent.com/11300712/40904365-816b1866-6815-11e8-92f1-c27c75dd929d.JPG)

```
import pyodbc
server ='wonseokjung.database.windows.net'
database='wonseokjung'
username='wonseokjung'
password='Ahf12dlq'
driver= '{ODBC Driver 13 for SQL Server}'
cnxn = pyodbc.connect('DRIVER='+driver+';SERVER='+server+';PORT=1443;DATABASE='+database+';UID='+username+';PWD='+ password)
cursor = cnxn.cursor()
```

```
driver= '{ODBC Driver 13 for SQL Server}'
cnxn = pyodbc.connect('DRIVER='+driver+';SERVER='+server+';PORT=1443;DATABASE='+database+';UID='+username+';PWD='+ password)
cursor = cnxn.cursor()
```
`conn = pymssql.connect(server='yourserver.database.windows.net', user='yourusername@yourserver', password='yourpassword', database='AdventureWorks')`


![23](https://user-images.githubusercontent.com/11300712/40948142-93b895c0-68a1-11e8-9822-cda7ed41351b.JPG)



![2](https://user-images.githubusercontent.com/11300712/40948143-93e20982-68a1-11e8-9b2f-19e201825053.JPG)



---

## references


3 단계: pymssql를 사용 하 여 SQL에 연결 하는 개념 증명

https://docs.microsoft.com/ko-kr/sql/connect/python/pymssql/step-3-proof-of-concept-connecting-to-sql-using-pymssql?view=sql-server-2017


마이크로소프트 설명 

https://docs.microsoft.com/en-us/azure/sql-database/sql-database-get-started-portal


Azure 사용하여 python 연결

https://docs.microsoft.com/ko-kr/azure/sql-database/sql-database-connect-query-python
