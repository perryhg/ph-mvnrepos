# ph-mvnrepos 
## deploy file to repo:
```Shell
mvn -DaltDeploymentRepository=snapshot-repo::default::file:../mvn-repository/releases clean deploy
```
if wish source or api being added, can add following to the mvn command arguments
```
mvn ... source:jar javadoc:jar
```

## usage

add repository config into your maven project pom.xml.

```xml
<repositories>
    <repository>
	<id>perryhg-mvn-repository</id>
	<url>https://raw.github.com/perryhg/ph-mvnrepos/master/releases</url>
    </repository>
</repositories>
```

The repository contains following artifacts:
```xml
<dependency>
	<groupId>com.lowagie</groupId>
	<artifactId>itext</artifactId>
	<version>2.1.7</version>
</dependency>

<dependency>
	<groupId>org.olap4j</groupId>
	<artifactId>olap4j</artifactId>
	<version>0.9.7.309-JS-3</version>
</dependency>

<dependency>
    <groupId>org.v66</groupId>
    <artifactId>qrhelper</artifactId>
    <version>0.1.1</version>
</dependency>

<dependency>
	<groupId>weibo</groupId>
	<artifactId>weibo4j-oauth2</artifactId>
	<version>beta3.1.1</version>
</dependency>
```