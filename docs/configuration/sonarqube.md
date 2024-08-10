---
sidebar_position: 4
---

# Setting up Sonarqube

## Download SonarQube

- ### Looking for SonarQube software Click here [SonarQube](https://www.sonarsource.com/products/sonarqube/downloads/historical-downloads).

`Note: Download SonarQube based on your Java version. For Example: If Java 17 is installed in your system then download SonarQube 10.6 version.`

## Go to Pom.xml in your application

- ### Step 1: Add properties in Pom.xml, For example refer below

```
	<properties>
		<java.version>17</java.version>
		<sonarqube.version>3.0.0.702</sonarqube.version>
		<!-- Define JaCoCo version -->
		<jacoco.version>0.8.8</jacoco.version>
		<sonar.exclusions>
            **/com/<your group name>/<your artifact name>/dto/**,
            **/com/<your group name>/<your artifact name>/entity/**,
            **/com/<your group name>/<your artifact name>/exception/**,
            **/com/<your group name>/<your artifact name>/repository/**,
            **/<your Application name>.java
        </sonar.exclusions>
	</properties>

```

- ### Step 2: Add `Jacoco` dependency in Pom.xml

```
    <dependency>
		<groupId>org.jacoco</groupId>
    	 <artifactId>jacoco-maven-plugin</artifactId>
		<version>0.8.8</version>
    </dependency>
```

- ### Step 3: Add `Plugins` in Pom.xml

```
 <!-- SonarQube plugin configuration -->
	    <plugin>
<groupId>org.sonarsource.scanner.maven</groupId>
<artifactId>sonar-maven-plugin</artifactId>
<version>${sonarqube.version}</version>
	   </plugin>
<!-- JaCoCo plugin configuration -->
	<plugin>
	<groupId>org.jacoco</groupId>
	<artifactId>jacoco-maven-plugin</artifactId>
	<version>${jacoco.version}</version>
	<executions>
		<execution>
			<goals>
			<goal>prepare-agent</goal>
			</goals>
    	        </execution>
		<execution>
		  <id>report</id>
		   <phase>prepare-package</phase>
			<goals>
			<goal>report</goal>
			</goals>
               </execution>
	</executions>
	<configuration></configuration>
	</plugin>
```

### Go to the SonarQube download folder

- open **bin** folder, if your using windows machine,then open **windows-x86-64**
- Click `StartSonar.bat`.
- Another Way to start sonar, Open **Command Prompt**, Type `StartSonar.bat` and Press **Enter**.
- Once the **SonarQube is operational** follow the next step.

### Go to the Browser

- Type `http://locahost:9000` and press **Enter**.
- Click on **Administration** , then click on the **security** tab. select the **users** in the dropdown.
- Click on the **Tokens** , Enter the **name** `for example: user` and click **Generate**, store the token for future purpose.

### Go to the Project directory

- Open **Command Prompt** and Type `mvn clean install`
- After Build Success, Type `mvn sonar:sonar -DSonar.token=<paste your generated token>` and Press **Enter**.
- if **Coverage** is not shown, try this command `mvn org.jacoco:jacoco-maven-plugin:prepare-agent install` in the **Command prompt**.
