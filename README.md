The Quiz Application backend is developed using Spring Boot, providing essential services for managing quizzes, questions, and user interactions. It acts as the core engine for creating and evaluating quizzes efficiently while ensuring secure access to resources.

Steps to Run the Quiz Application Backend (Spring Boot) with H2 Database:
1. Set Up the Development Environment

    Ensure Java Development Kit (JDK) 8 or higher is installed.
    Install necessary tools like IntelliJ IDEA, Eclipse, or a text editor like VSCode.

2. Clone the Repository

    Clone the Quiz Application repository from GitHub:

    git clone <repository-url>
    cd quiz-application

3. Import the Project into an IDE (Optional but Recommended)

    Open the project using your preferred IDE (IntelliJ IDEA, Eclipse, or VSCode).
    Import the project as a Maven or Gradle project.

4. Check the Dependencies and Configuration

    Verify if the pom.xml (for Maven) or build.gradle (for Gradle) has the required dependencies:

<!-- Maven dependency for Spring Boot and H2 Database -->
<dependencies>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-web</artifactId>
    </dependency>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-data-jpa</artifactId>
    </dependency>
    <dependency>
        <groupId>com.h2database</groupId>
        <artifactId>h2</artifactId>
        <scope>runtime</scope>
    </dependency>
</dependencies>

5. Configure the H2 Database in application.properties

    Ensure the H2 database configuration is correctly set in application.properties:

spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.driver-class-name=org.h2.Driver
spring.datasource.username=sa
spring.datasource.password=password
spring.h2.console.enabled=true
spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
spring.jpa.hibernate.ddl-auto=update

6. Run the Application

    Navigate to the project directory.
    Run the application using Maven:

mvn spring-boot:run

Or using Gradle:

    ./gradlew bootRun

7. Verify Application is Running

    The application should start successfully on http://localhost:8080.
    Check logs to ensure no errors are reported.

8. H2 Console Access for Database Interaction (Optional)

    If needed, access the H2 Console:
        Open your browser and go to: http://localhost:8080/h2-console.
    Use the following credentials:
        Username: sa
        Password: password

9. Test the APIs

    Ensure the required REST endpoints for quizzes and questions are working as expected.
    Use tools like Postman or curl to interact with the APIs.





1.Key Functionalities

    -> Manage Quizzes: Add, modify, view, or delete quiz data seamlessly.
    ->Handle Questions: Efficiently insert, update, or remove questions linked to quizzes.
    ->User Participation: Record and analyze user-submitted answers to quiz questions.
    ->API Security: Ensure secure access to endpoints through token-based authentication (e.g., JWT).(Best Feature)

2.Tech Stack

    ->Spring Boot Framework: A robust framework for building Java-based applications.(Backend)
    ->H2 Database: A lightweight, in-memory database for fast prototyping and testing.(DB)
    ->Spring Security: Provides advanced features for API protection.(Privacy & Security)

3.Database Configuration



# H2 Database Configuration
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.driver-class-name=org.h2.Driver
spring.datasource.username=sa
spring.datasource.password=password
spring.h2.console.enabled=true
spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
spring.jpa.hibernate.ddl-auto=update

4.Details:

    ->In-memory Database: H2 provides a transient database (jdbc:h2:mem:testdb) that is recreated each time the application restarts.
    ->H2 Console: Enabled for debugging purposes (http://localhost:8080/h2-console).
    ->JPA Settings: Automatically create or update tables based on the entity definitions.

5.Advantages of Using H2(Better use case)

    1.Lightweight: Requires no external installation or setup.
    2.Fast Development: Ideal for quick prototyping and testing.
    3.Embedded Mode: Runs as part of the application process, reducing external dependencies.
