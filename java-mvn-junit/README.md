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

### Post-Archetype Adjustments
After generating the quickstart project, two plugins were added manually to `pom.xml`:

1. `maven-compiler-plugin` (release 17) – Ensures the code is compiled targeting Java 17 consistently across different environments.
2. `exec-maven-plugin` – Configures a convenient way to run the app via `mvn exec:java` without crafting a manual `java -cp ...` command. It is set with `mainClass = com.example.app.App`.

These additions make the project immediately runnable for interviews or coding dojos with a single Maven command after compilation.

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
mvn compile exec:java
```

Notes:
- The `compile` phase is required the first time (or after code changes) so that classes exist under `target/classes` before the exec goal runs.
- After a successful compile (and if you haven't changed source files), you can just run:
	```sh
	mvn exec:java
	```
- For a clean rebuild (e.g., after pulling fresh changes) you can do:
	```sh
	mvn clean compile exec:java
	```

## Running Tests
Run all tests with Maven:
```sh
mvn test
```

---

This bootstrap is designed for quick setup and reliable testing in interviews and coding dojos. Feel free to extend it for your needs.
