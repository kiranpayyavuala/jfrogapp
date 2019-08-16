# jfrogapp

IN MAVEN SETTING.XML ADD THE BELOW SERVER TAG
---------------------------------------------
```
   <server>
      <id>snapshots</id>
      <username>admin</username>
      <password>TOKEN</password>
   </server>
```

ADD THIS ON POM.XML
-------------------
```
<distributionManagement>
    <repository>
        <id>central</id>
        <name>jfrog-releases</name>
        <url>http://OUR JFROG SERVER IP:8081/artifactory/example-repo-local</url>
    </repository>
    <snapshotRepository>
        <id>snapshots</id>
        <name>jfrog-snapshots</name>
        <url>http://OUR JFROG SERVER IP:8081/artifactory/example-repo-local</url>
    </snapshotRepository>
</distributionManagement>
```
```
<plugin>
   <artifactId>maven-deploy-plugin</artifactId>
   <version>2.8.1</version>
   <executions>
      <execution>
         <id>default-deploy</id>
         <phase>deploy</phase>
         <goals>
            <goal>deploy</goal>
         </goals>
      </execution>
   </executions>
   </plugin>
   ```
