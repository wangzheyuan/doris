## SelectDB For Apache Doris 发行包使用说明

SelectDB For Apache Doris 发行版，为了方便用户安装使用，我们在发行包中内置了JDK8，用户不需要再单独安装JDK，配置系统环境变量.

### 发行版安装包包含以下内容：

1. FE
2. BE
3. Broker
4. audit_loader
5. java8
6. jdbc_drivers 

### 安装包目录结构如下：

```
|-- apache_hdfs_broker
|   |-- LICENSE-dist.txt
|   |-- NOTICE.txt
|   |-- bin
|   |-- conf
|   |-- lib
|   `-- licenses
|-- audit_loader
|   `-- auditloader.zip
|-- be
|   |-- LICENSE-dist.txt
|   |-- NOTICE.txt
|   |-- bin
|   |-- conf
|   |-- lib
|   |-- licenses
|   |-- log
|   |-- storage
|   `-- www
|-- fe
|   |-- LICENSE-dist.txt
|   |-- NOTICE.txt
|   |-- bin
|   |-- conf
|   |-- doris-meta
|   |-- lib
|   |-- licenses
|   |-- log
|   |-- spark-dpp
|   `-- webroot
|-- java8
|   |-- COPYRIGHT
|   |-- LICENSE
|   |-- README.html
|   |-- THIRDPARTYLICENSEREADME-JAVAFX.txt
|   |-- THIRDPARTYLICENSEREADME.txt
|   |-- bin
|   |-- include
|   |-- javafx-src.zip
|   |-- jdk1.8.0_351
|   |-- jmc.txt
|   |-- jre
|   |-- legal
|   |-- lib
|   |-- man
|   |-- release
|   `-- src.zip
|-- jdbc_drivers
|   |-- clickhouse-jdbc-0.3.2-patch11-all.jar
|   |-- mssql-jdbc-11.2.0.jre8.jar
|   |-- mysql-connector-java-8.0.25.jar
|   |-- ojdbc6.jar
|   `-- postgresql-42.5.0.jar
`-- udf
    |-- include
    `-- lib
```
说明：
1. JDBC 驱动程序用于 JDBC 外部表或 JDBC Muitl Catalog功能。 所有的驱动都保存在安装包根目录下jdbc_drivers
2. java8 是用于 fe、be、apache_hdfs_broker 运行所必须得 Java 运行环境，如果用户没有在所有节点安装 Java 运行环境并配置 JAVA_HOME  系统环境变量，系统将默认使用这个默认的 Java 运行环境。

### 安装使用

具体的安装方法，参照官网安装手册：[安装与部署 - Apache Doris](https://doris.apache.org/zh-CN/docs/dev/install/install-deploy)

为了方便用户安装使用，避免繁杂 Java 系统环境变量设置，我们直接内置了JDK，用户只需要将安装包解压，直接运行相对应目录下的启动脚本即可。

**注意： 发行版安装包下的 java8 目录不能删除，不能改变目录**