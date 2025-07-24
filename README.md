# Jenkins Pipeline: Maven Build and Java App Deployment

This repository contains a Jenkins pipeline that automates the build, test, packaging, and deployment of a Java application using Maven.

## 🔄 Pipeline Stages

1. **Build**
   - Cleans and compiles the source code using Maven:
     ```bash
     mvn clean compile
     ```

2. **Test**
   - Executes unit tests:
     ```bash
     mvn test
     ```

3. **Package**
   - Packages the compiled application into a JAR file:
     ```bash
     mvn package
     ```

4. **Deploy**
   - Runs the packaged Java application with a sample argument:
     ```bash
     java -cp target/your-app-1.0-SNAPSHOT.jar com.apasoft.ToUpper "example test"
     ```

## ☑️ Requirements

- Jenkins with shell access.
- Maven and JDK installed on the Jenkins agent.
- A Java application with:
  - `pom.xml` configured for Maven.
  - Main class: `com.apasoft.ToUpper`.

## 📌 Notes

- Update `your-app-1.0-SNAPSHOT.jar` and the main class path as needed.
- The deploy step is currently configured with a static input (`"example test"`), which can be customized per use case.
