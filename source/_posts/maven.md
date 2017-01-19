---
title: maven
date: 2017-01-19 11:22:09
tags:
---
# maven

#### maven编译的时候跳过test
1. 用命令带上参数
```bash
 mvn install -Dmaven.test.skip=true
```
2. 在pom.xml里面配置
```xml
<plugins>
      <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-surefire-plugin</artifactId>
        <configuration>
          <skip>true</skip>
        </configuration>
      </plugin>
</plugins>
```
