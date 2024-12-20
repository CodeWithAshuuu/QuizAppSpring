The Quiz Application backend is developed using Spring Boot, providing essential services for managing quizzes, questions, and user interactions. It acts as the core engine for creating and evaluating quizzes efficiently while ensuring secure access to resources.


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