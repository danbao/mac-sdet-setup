# DBeaver

作为一名开发者，我们常常需要连接管理数据库。这些数据库类型类型众多，形式多样。为了方便管理这些数据库我们选择DBeaver， 它是一个通用的数据库管理工具和 SQL 客户端，支持 MySQL, PostgreSQL, Oracle, DB2, MSSQL, Sybase, Mimer, HSQLDB, Derby, 以及其他兼容 JDBC 的数据库。

先去[官网](https://dbeaver.io/download/)下载 **DBeaver Community**版，下载完成后将 **DBeaver** 拖拽进入 Application 文件夹中。然后，你可以在 **Launchpad** 中启动 DBeaver。

或者选择使用`brew cask`安装

```bash
    $ brew cask install dbeaver-community
```

## 配置jdbc driver 来连接Oracle数据库

先去下载 [Oracle Database JDBC driver](https://www.oracle.com/technetwork/database/application-development/jdbc/downloads/index.html)

然后在`iTerm`执行以下命令

```bash
    $ cd ~/.dbeaver-drivers/
    $ tar -zxvf ~/Downloads/ojdbc8-full.tar.gz
    $ cd ojdbc8-full
    $ pwd
    $ ls -la
```

显示的结果如下

```bash
➜  ojdbc8-full pwd
/Users/hello/.dbeaver-drivers/ojdbc8-full
➜  ojdbc8-full ls -la
total 16640
drwx------@ 13 hello  staff      416 Aug 21 04:29 .
drwxr-xr-x   3 hello  staff       96 Nov 18 13:53 ..
-rw-r--r--@  1 hello  staff     2595 Aug 21 04:29 README.txt
-r-xr-xr-x@  1 hello  staff    11596 Aug  3 05:25 ojdbc.policy
-r--r--r--@  1 hello  staff  4161744 Aug  3 05:25 ojdbc8.jar
-r--r--r--@  1 hello  staff   144428 Aug  3 05:25 ons.jar
-r--r--r--@  1 hello  staff   307817 Aug  3 05:25 oraclepki.jar
-r--r--r--@  1 hello  staff  1661545 Aug  3 05:25 orai18n.jar
-r--r--r--@  1 hello  staff   205152 Aug  3 05:25 osdt_cert.jar
-r--r--r--@  1 hello  staff   306854 Aug  3 05:25 osdt_core.jar
-r--r--r--@  1 hello  staff    29103 Aug  3 05:25 simplefan.jar
-r--r--r--@  1 hello  staff  1398331 Aug  3 05:25 ucp.jar
-r--r--r--@  1 hello  staff   262415 Aug  3 05:25 xdb6.jar
```

接着在`${HOME}/.dbeaver4/.metadata/.plugins/org.jkiss.dbeaver.core/drivers.xml`文件中写入以下内容（如文件不存在，则新建一个）
```xml
<?xml version="1.0" encoding="UTF-8"?>
<drivers>

    <provider id="oracle">
        <driver id="oracle_thin" category="Oracle" custom="false" embedded="false" name="Oracle" class="oracle.jdbc.OracleDriver"
            url="jdbc:oracle:thin:@{host}[:{port}]/{database}" port="1521" description="Oracle thin driver. Doesn&#39;t require Oracle client.">
            <library type="jar" path="${HOME}/.dbeaver-drivers/ojdbc8-full/ojdbc8.jar" custom="true" />
            <library type="jar" path="${HOME}/.dbeaver-drivers/ojdbc8-full/orai18n.jar" custom="true" />
            <library type="jar" path="${HOME}/.dbeaver-drivers/ojdbc8-full/xdb6.jar" custom="true" />
            <library type="jar" path="${HOME}/.dbeaver-drivers/ojdbc8-full/ons.jar" custom="true" />
            <library type="jar" path="${HOME}/.dbeaver-drivers/ojdbc8-full/oraclepki.jar" custom="true" />
            <library type="jar" path="${HOME}/.dbeaver-drivers/ojdbc8-full/osdt_cert.jar" custom="true" />
            <library type="jar" path="${HOME}/.dbeaver-drivers/ojdbc8-full/osdt_core.jar" custom="true" />
            <library type="jar" path="${HOME}/.dbeaver-drivers/ojdbc8-full/simplefan.jar" custom="true" />
            <library type="jar" path="${HOME}/.dbeaver-drivers/ojdbc8-full/ucp.jar" custom="true" />
        </driver>
    </provider>

</drivers>
```

这样就可以正常的连接Oracle数据库啦

更多设置可以参考DBeaver 的 [Wiki Page](https://github.com/dbeaver/dbeaver/wiki/Admin-Manage-Drivers)。