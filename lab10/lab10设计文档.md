# lab10
## Exercise7
#### 1.PDO

![](F:\GITHUB\SOFT130002_lab\lab10\images\1.jpg)

```
分别通过 $pdo = new PDO(DBCONNSTRING,DBUSER,DBPASS); 和 $pdo = null;连接数据库或断开连接。
```

```
通过 $pdo->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);和catch来处理异常
```

```
$sql = "select * from Artists order by LastName";设置选择形式并接下来输出结果
```
#### 2.mysqli

![](F:\GITHUB\SOFT130002_lab\lab10\images\2.jpg)

```
通过$connection = mysqli_connect(DBHOST, DBUSER, DBPASS, DBNAME);和mysqli_close($connection);创建和断开数据库连接
```

```
$sql = "select * from Genres order by GenreName";设置选择形式
```
用若干判断语句确定连接情况和循环情况

## Exercise8

![](F:\GITHUB\SOFT130002_lab\lab10\images\3.jpg)

#### 1.outputArtists()

与前一个exercise大体相同，之后while循环中把LastName在a标签输出，并用if语句进行了判断。

#### 2.outputPaintings()

与之前的大体相同，while循环中为outputSinglePainting函数

#### 3.outputSinglePainting($row)

用php输出单张图片

一、执行sql语句的方式

1、ResultSet  executeQuery（String sql）throws SQLException：专用于查询。

2、int  executeUpdate（String sql）throws SQLException：执行DDL、DML语句，前者返回0，后者返回受影响行数。

3、boolean execute（String sql）throws SQLException：可执行任何SQL 语句。如果执行后第一个结果为ResultSet（即执行了查询语句），则返回true；如果执行了DDL、DML语句，则返回false。返回结果为true，则随后可通过该Statement对象的getResultSet()方法获取结果集对象（ResultSet类型），返回结果为false，则可通过Statement对象的getUpdateCount（）方法获得受影响的行数。

二、PreparedStatement的好处

1、预编译SQL语句，性能更好，执行更快。

2、无须“拼接”SQL 语句，编程更简单。

3、可以防止SQL 注入（如将输入的true当成直接量，导致判断直接通过，从而降低了安全性），安全性更好。

## Exercise10

![](F:\GITHUB\SOFT130002_lab\lab10\images\4.jpg)

第一个函数整体和Exercise9中类似，通过$sql进行分类选择，catch来处理异常，以此实现分类检索。在while中用outputSingleGenre($row)函数。
而第二个函数就是通过php输出html来完成页面情况，其中具体点如图片页后生成的链接用constructGenreLink函数实现。

