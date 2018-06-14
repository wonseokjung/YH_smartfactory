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
 
 
# receive all data from data table

for 



python 연결

![sql](https://user-images.githubusercontent.com/11300712/40904365-816b1866-6815-11e8-92f1-c27c75dd929d.JPG)

```
import pyodbc
server ='wonseokjung.database.windows.net'
database='wonseokjung'
username='wonseokjung'
password='**'
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

### python과 서버 연동해서 data 추출 및 삽입 실험 완료 
 
![23](https://user-images.githubusercontent.com/11300712/40948142-93b895c0-68a1-11e8-9822-cda7ed41351b.JPG)


### Proto Type Server 구축 완료 

![2](https://user-images.githubusercontent.com/11300712/40948143-93e20982-68a1-11e8-9b2f-19e201825053.JPG)



---

# Thins to do 

1. 현재 ERP 와 연동   
- 
```
server ='wonseokjung.database.windows.net'
database='wonseokjung'
username='wonseokjung'
password='**'
driver= '{ODBC Driver 13 for SQL Server}'
```
- 어떤 server를 쓰는가 ? 
- python과 연동 가능한가? 
 

---

2. 현재 서버에 Image, PDF, GIF 등 Text가 아닌 File이 저장 및 import가 가능한가? 

- 가능하다면 : 속도는 어느정도 걸릴것인가 ? 

- 가능하지 않다면 : 다른 서버를 만들어야 하는 것인가 ? , 어떤 방법이 있을까? 

3. 

---

## references


3 단계: pymssql를 사용 하 여 SQL에 연결 하는 개념 증명

https://docs.microsoft.com/ko-kr/sql/connect/python/pymssql/step-3-proof-of-concept-connecting-to-sql-using-pymssql?view=sql-server-2017


마이크로소프트 설명 

https://docs.microsoft.com/en-us/azure/sql-database/sql-database-get-started-portal


Azure 사용하여 python 연결

https://docs.microsoft.com/ko-kr/azure/sql-database/sql-database-connect-query-python
