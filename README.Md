
# 框架说明
- 采用SpringBoot+Mybatis+Hutool工具栏+Ueboot(自定义框架:包含用户登录校验、基础类、工具类)+Redis+MySQL
- ueboot-dependencies 声明所有ueboot-cloud模块的版本号及依赖的第三方组件版本号
  - 项目主要通过引入这个配置即可
```xml
    <parent>
        <groupId>com.ueboot.cloud</groupId>
        <artifactId>ueboot-dependencies</artifactId>
        <version>1.2.0-SNAPSHOT</version>
        <relativePath/>
    </parent>

```
- ueboot-framework 包含了所有核心的功能模块，可以按需引入
- ueboot-system 主要用于后台管理系统当中涉及到用户管理、角色管理、权限管理功能

## 注意实现
## 开发注意配置
- 需要先配置maven的中央仓库用于下载ueboot开发框架相关的jar和源码。可以在本地maven的settings文件当中增加如下内容
```xml
 <profiles>
        <profile>
            <id>ueboot-cloud</id>
            <activation>
                <activeByDefault>true</activeByDefault>
            </activation>
            <repositories>
                <repository>
                    <id>ueboot-release</id>
                    <name>public</name>
                    <url>https://maven.xiqiao.io/content/groups/public/</url>
                    <releases>
                        <enabled>true</enabled>
                    </releases>
                    <snapshots>
                        <enabled>true</enabled>
                    </snapshots>
                </repository>
            </repositories>
            <pluginRepositories>
                <pluginRepository>
                    <id>ueboot-release</id>
                    <name>public</name>
                    <url>https://maven.xiqiao.io/content/groups/public/</url>
                    <releases>
                        <enabled>true</enabled>
                    </releases>
                    <snapshots>
                        <enabled>true</enabled>
                    </snapshots>
                </pluginRepository>
            </pluginRepositories>
        </profile>
    </profiles>
```


# 参考文档
部分使用文档
https://www.wolai.com/youidian/oaB2exa61fa1jdcQFKfaJe


## 版本说明
- development 等价于 1.1.0
- 1.2.0 最新代码
- master 无用


# 更新记录

#### 2022-04-15

1. 版本更新 SpringBoot 2.6.6
2. 版本更新 SpringCloud 2021.0.1
3. 版本更新 SpringCloudAlibaba 2021.0.1.0
4. 版本更新 Mybatis-Plus 3.5.1
5. 版本更新 Dynamic Datasource 3.5.1
6. 版本更新 SaToken 1.29.0
7. 移除部分无用依赖和属性
8. 更新版本号 1.1.1-SNAPSHOT
9. 新增应用纬度Profiles，用于指定应用配置文件加载