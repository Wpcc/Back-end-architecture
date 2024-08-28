# Maven

**Maven是apache旗下的一个开源项目，是一款用于管理和构建java项目的工具。**

作用：

- 依赖管理：管理依赖的jar包，方便后续升级
- 统一的项目结构：适合不同的编辑器开发
- 项目构建：标准跨平台的自动化项目构建方式

![2024-08-28_224642](.\static\2024-08-28_224642.png)

### 安装

- 解压apache-maven-3.6.1-bin.zip

- 配置本地仓库：修改conf/settings.xml中的`<localRepository>`为一个指定目录

  ```xml
  <localRepository>E:\develop\apache-maven-3.6.1\mvn_repo</localRepository>
  ```

- 配置阿里云私服：修改conf\settings.xml中的`<mirrors>`标签，为其添加如下子标签：

  ```xml
  <mirror>
      <id>alimaven</id>
      <name>aliyun maven</name>
      <url>http://maven.aliyun.com/nexus/content/groups/public/</url>
      <mirrorOf>central</mirrorOf>
  </mirror>
  ```

- 配置环境变量：MAVEN_HOME为maven的解压目录，并将其bin目录加入PATH环境变量

- 配置完毕：通过`mvn -v`查看是否配置成功

### IEDA集成Maven

#### 配置Maven环境（本地项目）

- 选择 IDEA 中的FILE --> Settings --> Build,Execution,Deployment --> Build Tools --> Maven

- 设置 IDEA 使用本地安装的 Maven，并修改配置文件及本地仓库路径

  - Maven home path
  - User settings file
  - Local repository

- 查看Maven--> Runner中的JRE是否为当前版本

- 配置Java的字节码版本 Compiler中的Project bycode version

  

#### 配置Maven环境（所有）

- 选择File --》 close Project
- 选择Customize --》all Settings
- 同上

仅对未创建的项目生效

#### 创建Maven项目

#### 导入Maven项目

