JDBC

### 简介
JDBC(Java Database Connectivity)

### 配置
下载驱动包： mysql-connector-java
https://mvnrepository.com/artifact/mysql/mysql-connector-java
```xml
<dependency>
    <groupId>mysql</groupId>
    <artifactId>mysql-connector-java</artifactId>
    <version>8.0.22</version>
</dependency>
```
or
```groovy
compile group: 'mysql', name: 'mysql-connector-java', version: '8.0.22'
```

### 连接
```java
Class.forName("com.mysql.cj.jdbc.Drive");
Connection connection = DriverManager.getConnection("jdbc:mysql://localhost:3306/test", "root", "123");
Statement statement = connection.createStatement();
ResultSet rs = statement.executeQuery("SELECT * FROM user");
while (rs.next()) {
    System.out.println("姓名：" + rs.getString("name") + " 年龄：" + rs.getInt("age"));
}
rs.close();
statement.close();
connection.close();
```