# CI-Project
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <groupId>com.microsoft</groupId>
	<artifactId>ROOT</artifactId>
	<version>1.0</version>
	<packaging>war</packaging>
	<name>Sample Spring App</name>
    <parent>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-parent</artifactId>
        <version>1.5.7.RELEASE</version>
    </parent>
	<repositories>
       <repository>
          <id>central</id>
          <name>Central</name>
          <url>https://repo1.maven.org/maven2</url>
       </repository>
    </repositories>
    <dependencies>
        <dependency>
			<groupId>com.microsoft.azure</groupId>
			<artifactId>applicationinsights-web</artifactId>
			<!-- or applicationinsights-core for bare API -->
			<version>[1.0,)</version>
		</dependency>
		<dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-web</artifactId>
        </dependency>    		
    </dependencies>

    <properties>
        <java.version>1.8</java.version>
    </properties>

    <build>
	<finalName>ROOT</finalName>
        <plugins>
            <plugin>
                <groupId>org.springframework.boot</groupId>
                <artifactId>spring-boot-maven-plugin</artifactId>
            </plugin>
            <plugin>
                <artifactId>maven-failsafe-plugin</artifactId>
                <executions>
                    <execution>
                        <goals>
                            <goal>integration-test</goal>
                            <goal>verify</goal>
                        </goals>
                    </execution>
                </executions>
            </plugin>
        </plugins>
    </build>

</project>
Footer
