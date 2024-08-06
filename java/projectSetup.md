## How to add JDBC Drivers to a Maven Project
### JDBC - Java Database Connectivity driver is a software component that allows Java apps to interact with databases.
- Go to https://mvnrepository.com/artifact/org.postgresql/postgresql/42.7.3 to find the correct driver. In this case the link goes to PostgreSQL JDBC Driver
- Click on the Version e.g. 42.7.3
- Copy the dependency code like below and past into the pom.xml file of your project.
- The dependency JDBC driver into should be wrapped inside of ```<dependencies>``` 
and add the postgres info inside of ```<properties>```

```
    <properties>
        <java.version>21</java.version>
        <postgres.jdbc.version>${postgres.jdbc.version}</postgres.jdbc.version>
    </properties>
    
    <dependencies>
        <dependency>
            <groupId>org.postgresql</groupId>
            <artifactId>postgresql</artifactId>
            <version>42.7.3</version>
        </dependency>
    </dependencies>
```
- In intellij  reload Maven Changes and Run the project to make sure the JDBC driver is working correctly.