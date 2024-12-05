---
layout: post
title: "JDBC连接Oracle11g（附jar包）"
date:   2023-01-02
tags: [数据库,Oracle,JDBC,连接,jar]
comments: true
author: admin
---
# JDBC连接Oracle11g（附jar包）

## 介绍

本资源文件提供了使用JDBC连接Oracle 11g数据库所需的jar包及相关配置说明。通过本资源，您可以轻松地在Java应用程序中实现与Oracle 11g数据库的连接，并执行各种数据库操作。

## 内容

- **ojdbc6.jar**: Oracle 11g的JDBC驱动包，适用于JDK 6及以上版本。
- **配置说明**: 详细介绍了如何在Java项目中配置和使用JDBC连接Oracle 11g数据库。

## 使用步骤

1. **导入jar包**: 将`ojdbc6.jar`文件添加到您的Java项目的`lib`目录中，并在构建路径中引用该jar包。
2. **注册驱动**: 使用`Class.forName("oracle.jdbc.driver.OracleDriver")`方法注册Oracle JDBC驱动。
3. **连接数据库**: 使用`DriverManager.getConnection(url, user, password)`方法获取数据库连接。
4. **执行SQL**: 使用`Statement`或`PreparedStatement`对象执行SQL语句。
5. **关闭资源**: 在操作完成后，确保关闭`ResultSet`、`Statement`和`Connection`对象，以释放资源。

## 示例代码

以下是一个简单的JDBC连接Oracle 11g数据库的示例代码：

```java
import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.PreparedStatement;
import java.sql.ResultSet;
import java.sql.SQLException;

public class OracleJdbcExample {
    public static void main(String[] args) {
        Connection conn = null;
        PreparedStatement ps = null;
        ResultSet resultSet = null;

        try {
            // 加载Oracle驱动
            Class.forName("oracle.jdbc.driver.OracleDriver");

            // 数据库连接信息
            String url = "jdbc:oracle:thin:@127.0.0.1:1521:orcl";
            String user = "scott";
            String password = "tiger";

            // 获取连接
            conn = DriverManager.getConnection(url, user, password);

            // 预编译SQL语句
            String sql = "SELECT * FROM student WHERE name = ?";
            ps = conn.prepareStatement(sql);
            ps.setString(1, "小李");

            // 执行查询
            resultSet = ps.executeQuery();

            // 处理结果集
            while (resultSet.next()) {
                System.out.println(resultSet.getString("age"));
            }
        } catch (Exception e) {
            e.printStackTrace();
        } finally {
            // 关闭资源
            try {
                if (resultSet != null) resultSet.close();
                if (ps != null) ps.close();
                if (conn != null) conn.close();
            } catch (SQLException e) {
                e.printStackTrace();
            }
        }
    }
}
```

## 注意事项

- 确保您的Oracle 11g数据库已正确安装并运行。
- 根据实际情况调整数据库连接信息（如URL、用户名和密码）。
- 在生产环境中，建议使用连接池技术（如HikariCP、C3P0等）来管理数据库连接，以提高性能和资源利用率。

通过本资源文件，您可以快速上手使用JDBC连接Oracle 11g数据库，并进行各种数据库操作。希望本资源对您的开发工作有所帮助！

## 下载链接

[JDBC连接Oracle11g附jar包分享](https://pan.quark.cn/s/59b6a9e36f15)