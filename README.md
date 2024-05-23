# CK_Student_GV
# Class Diagram:
![image](https://github.com/KittoLapTrinh/CK_Student_GV/assets/96908923/22909a2f-1238-4581-9f24-a21f3fef5c1e)
# Database Diagram:
![image](https://github.com/KittoLapTrinh/CK_Student_GV/assets/96908923/7c861086-ac02-4d42-9224-660191d773ff)

# pom.xml
```
<dependencies>

		<!-- https://mvnrepository.com/artifact/org.hibernate/hibernate-core -->
		<dependency>
			<groupId>org.hibernate</groupId>
			<artifactId>hibernate-core</artifactId>
			<version>6.4.4.Final</version>
		</dependency>

		<!-- https://mvnrepository.com/artifact/org.hibernate/hibernate-testing -->
		<dependency>
			<groupId>org.hibernate</groupId>
			<artifactId>hibernate-testing</artifactId>
			<version>6.4.4.Final</version>
			<scope>test</scope>
		</dependency>

		<!--
		https://mvnrepository.com/artifact/org.junit.jupiter/junit-jupiter-api -->
		<dependency>
			<groupId>org.junit.jupiter</groupId>
			<artifactId>junit-jupiter-api</artifactId>
			<version>5.10.2</version>
			<scope>test</scope>
		</dependency>

		<!--
		https://mvnrepository.com/artifact/org.junit.jupiter/junit-jupiter-engine -->
		<dependency>
			<groupId>org.junit.jupiter</groupId>
			<artifactId>junit-jupiter-engine</artifactId>
			<version>5.10.2</version>
			<scope>test</scope>
		</dependency>
		
		<!--
		https://mvnrepository.com/artifact/com.microsoft.sqlserver/mssql-jdbc -->
		<dependency>
			<groupId>com.microsoft.sqlserver</groupId>
			<artifactId>mssql-jdbc</artifactId>
			<version>12.3.0.jre20-preview</version>
		</dependency>
		
		<!-- https://mvnrepository.com/artifact/org.projectlombok/lombok -->
		<dependency>
			<groupId>org.projectlombok</groupId>
			<artifactId>lombok</artifactId>
			<version>1.18.30</version>
			<scope>provided</scope>
		</dependency>

		<!--
		https://mvnrepository.com/artifact/org.mariadb.jdbc/mariadb-java-client -->
		<dependency>
			<groupId>org.mariadb.jdbc</groupId>
			<artifactId>mariadb-java-client</artifactId>
			<version>3.3.3</version>
		</dependency>

	</dependencies>
```

# persistence.xml:
```
	<persistence-unit name="JPA_ORM_Student MSSQL">
		<provider>org.hibernate.jpa.HibernatePersistenceProvider</provider>
		<properties>
			<property name="jakarta.persistence.jdbc.url"
				value="jdbc:sqlserver://localhost:1433;databaseName=StudentDB;trustServerCertificate=true" />
			<property name="jakarta.persistence.jdbc.user" value="sa" />
			<property name="jakarta.persistence.jdbc.password"
				value="sapassword" />
			<property name="jakarta.persistence.jdbc.driver"
				value="com.microsoft.sqlserver.jdbc.SQLServerDriver" />
				
			<property name="jakarta.persistence.jdbc.dialect"
				value="org.hibernate.dialect.SQLServerDialect" />
				
			<property name="hibernate.show_sql" value="true" />
			<property name="hibernate.format_sql" value="true" />
			<property name="hibernate.hbm2ddl.auto" value="update" />
		</properties>
	</persistence-unit>

	<persistence-unit name="JPA ORM MariaDB">

		<provider>org.hibernate.jpa.HibernatePersistenceProvider</provider>
		<properties>
			<property name="jakarta.persistence.jdbc.driver"
				value="org.mariadb.jdbc.Driver" />
			<property name="jakarta.persistence.jdbc.url"
				value="jdbc:mariadb://localhost:3306/testdb" />
			<property name="jakarta.persistence.jdbc.user" value="root" />
			<property name="jakarta.persistence.jdbc.password"
				value="root" />
				
			<property name="jakarta.persistence.jdbc.dialect"
				value="org.hibernate.dialect.MariaDBDialect" />
				
			<property name="hibernate.show_sql" value="true" />
			<property name="hibernate.format_sql" value="true" />
			<property name="hibernate.hbm2ddl.auto" value="update" />

		</properties>

	</persistence-unit>
```
