# gradle-gallery

A gallery of gradle tools. It compose of basic-java, easy-web, pro-web.

## Usage

```
git submodule add git@github.com:easyweb4j/gradle-gallery.git gradle/gallery
```


## Basic Java

Base Java is composed of basic java project settings, opinioned 3rd libs.

### Features

- use utf-8 file encoding
- set java compatibility 1.8
- add AutoValue annotation proccessor
- set timezone for test & java exec
- include jacoco report, default to html report
- use testNG framework, exclude junit4 & junit5

### Dependencies

- Guava:28.1-jre
- Apache Commons Lang:3.9
- Apache Commons Collection 4.4
- Apache Commons Codec:1.13
- Slf4j: 1.7.29
- AutoValue 1.7
- TestNG: 7.0.0

### Variables

| Variable                 | Default Value                  | Explaination                            |
| --                       | --                             | --                                      |
| fileEncoding             | UTF-8                          |                                         |
| sourceCompatibility      | 1.8                            |                                         |
| targetCompatibility      | 1.8                            |                                         |
| compilerArgs             | ['-Xlint:unchecked']           | compilation arguments                   |
| tz                       | UTC                            | test & runtime timezone                 |
| annonGenDir              | PROJECT_DIR/src/generated/java | annotationProcessor generated directory |
| guavaVersion             | 28.1-jre                       |                                         |
| commonsLangVersion       | 3.9                            |                                         |
| commonsCollectionVersion | 4.4                            |                                         |
| commonsCodecVersion      | 1.13                           |                                         |
| slf4jVersion             | 1.7.29                         |                                         |
| autoValueVersion         | 1.7                            |                                         |
| testNGVersion            | 7.0.0                          |                                         |


## MyBatis Generator
MyBatis Generator is composed of opinioned mybatis generator configuration and tasks easied for
configuration. 

### Tasks

#### generateMybatisConfigFile 

Generate mybatis configuration file to location set by variable **mybatisGenertorConfigFilePath**.

#### mybatisGenerateSrc

Execute the mybatis generation job.

Generate mybatis configuration file to location set by variable **mybatisGenertorConfigFilePath**.

### Variables

| Variable                 | Default Value                  | Explaination                            |
| --                       | --                             | --                                      |
|fileEncoding|UTF-8||
|mybatisGeneratorVersion|1.3.7|mybatis generator core version|
|mysqlConnectorVersion|8.0.18||
|mybatisVersion|3.5.3||
|hikariCPVersion|3.4.1|connection pool **hikariCP** version|
|dbConnectionProps|driverClass="com.mysql.cj.jdbc.Driver"<br/>jdbcUrl="jdbc:mysql://localhost:3306/devel?useUnicode=true&useSSL=false&characterEncoding=utf-8&useSSL=false&serverTimezone=UTC"<br
/>user='devel'<br/>password='123456'|a map set database connection properties|
|basePackage|com.example.generated.mybatis||
|overwrite|true|mybatis generator overwrite existing source code|
|useDefaultDriver|true|use default database driver **mysql**, default version check variable|**mysqlConnectorVersion**|
