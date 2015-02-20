# ph-mvnrepos 
## deploy file to repo:
```Shell
mvn -DaltDeploymentRepository=snapshot-repo::default::file:../mvn-repository/releases clean deploy
```
if wish source or api being added, can add following to the mvn command arguments
```Shell
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