# Java Maven JUnit Bootstrap

This folder contains a minimal Java Maven project for live coding, technical interviews, and coding dojos. It includes a simple application and a JUnit test, following best practices for Java development.

## Project Structure
- `pom.xml` — Maven project descriptor
- `src/main/java/com/example/app/App.java` — Main application class
- `src/test/java/com/example/app/AppTest.java` — JUnit test class

## How It Was Created
```
mvn archetype:generate -DgroupId=com.example.app -DartifactId=java-mvn-junit -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false
```

## Prerequisites
- [Java JDK 17+](https://adoptium.net/) installed
- [Apache Maven](https://maven.apache.org/download.cgi) installed

## Running in GitHub Codespaces
You can use this project directly in GitHub Codespaces for interviews or coding dojos. No local installation is required.

1. Fork this repository into your own account.
2. Create a new Codespace from your fork.
3. Open the `java-mvn-junit` folder in Codespaces.
4. Use the integrated terminal to run the setup and commands below.

## First-Time Setup
Restore dependencies before running or testing:
```sh
mvn install
```

## Running the App
Run the main class using Maven (make sure you are in the `java-mvn-junit` directory):
```sh
mvn exec:java -Dexec.mainClass=com.example.app.App
```

## Running Tests
Run all tests with Maven:
```sh
mvn test
```

---

This bootstrap is designed for quick setup and reliable testing in interviews and coding dojos. Feel free to extend it for your needs.
