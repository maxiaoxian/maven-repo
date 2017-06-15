# Git版Maven仓库

1、Deploy到本地仓库:

- 在Maven配置中，添加：
```
<distributionManagement>
    <repository>
        <id>carzyhc-mvn-repo</id>
        <url>file:D:/Program Files/apache-maven-3.5.0/local-repo/</url>
    </repository>
</distributionManagement>
```
- 执行Maven命令：
```
mvn clean package deploy -Dmaven.skip.test=true
```

2、在MAVEN工程中，添加:
```
<repositories>
    <repository>
        <id>carzyhc-mvn-repo</id>
        <url>https://raw.githubusercontent.com/maxiaoxian/maven-repo/master/</url>
    </repository>
</repositories>
```
