

# # Spring Boot All Annotations 

---

### **1. What is the `@SpringBootApplication` annotation in Spring Boot?**
- **Purpose**: Combines `@Configuration`, `@EnableAutoConfiguration`, and `@ComponentScan`.
- **Usage**: Marks the main class of a Spring Boot application.
- **Example**:
  ```java
  @SpringBootApplication
  public class MyApplication {
      public static void main(String[] args) {
          SpringApplication.run(MyApplication.class, args);
      }
  }
  ```

---

### **2. What is the `@EnableAutoConfiguration` annotation in Spring Boot?**
- **Purpose**: Enables Spring Boot's auto-configuration mechanism.
- **Usage**: Automatically configures the application based on the dependencies present in the classpath.
- **Example**:
  ```java
  @Configuration
  @EnableAutoConfiguration
  public class MyConfig {}
  ```

---

### **3. What is the `@ConditionalOnClass` annotation in Spring Boot?**
- **Purpose**: Configures a bean only if a specified class is present in the classpath.
- **Usage**: Used in auto-configuration classes.
- **Example**:
  ```java
  @Configuration
  @ConditionalOnClass(DataSource.class)
  public class DataSourceAutoConfiguration {}
  ```

---

### **4. What is the `@ConditionalOnMissingBean` annotation in Spring Boot?**
- **Purpose**: Configures a bean only if no bean of the specified type is already present in the application context.
- **Usage**: Used in auto-configuration classes.
- **Example**:
  ```java
  @Bean
  @ConditionalOnMissingBean
  public MyBean myBean() {
      return new MyBean();
  }
  ```

---

### **5. What is the `application.properties` file in Spring Boot?**
- **Purpose**: A configuration file for defining application properties.
- **Usage**: Stores key-value pairs for configuring the application.
- **Example**:
  ```properties
  server.port=8080
  spring.datasource.url=jdbc:mysql://localhost:3306/mydb
  ```

---

### **6. What is the `application.yml` file in Spring Boot?**
- **Purpose**: A YAML-based configuration file for defining application properties.
- **Usage**: Provides a more readable and structured format compared to `application.properties`.
- **Example**:
  ```yaml
  server:
    port: 8080
  spring:
    datasource:
      url: jdbc:mysql://localhost:3306/mydb
  ```

---

### **7. What is the difference between `application.properties` and `application.yml`?**
- **`application.properties`**:
  - Uses a key-value format.
  - Less readable for nested configurations.
- **`application.yml`**:
  - Uses YAML format.
  - More readable and structured for nested configurations.

---

### **8. What is the `@ConfigurationProperties` annotation in Spring Boot?**
- **Purpose**: Binds external configuration properties to a Java object.
- **Usage**: Used to create strongly-typed configuration classes.
- **Example**:
  ```java
  @ConfigurationProperties(prefix = "app")
  public class AppConfig {
      private String name;
      // Getters and setters
  }
  ```

---

### **9. What is the `@EnableConfigurationProperties` annotation in Spring Boot?**
- **Purpose**: Enables the use of `@ConfigurationProperties`-annotated classes.
- **Usage**: Registers configuration properties classes as beans.
- **Example**:
  ```java
  @Configuration
  @EnableConfigurationProperties(AppConfig.class)
  public class MyConfig {}
  ```

---

### **10. What is the `@SpringBootTest` annotation in Spring Boot?**
- **Purpose**: Used for integration testing of Spring Boot applications.
- **Usage**: Loads the full application context for testing.
- **Example**:
  ```java
  @SpringBootTest
  public class MyIntegrationTest {
      // Test methods
  }
  ```

---

### **11. What is the `@MockBean` annotation in Spring Boot?**
- **Purpose**: Adds a mock bean to the Spring application context.
- **Usage**: Used in tests to mock dependencies.
- **Example**:
  ```java
  @SpringBootTest
  public class MyTest {
      @MockBean
      private MyService myService;
  }
  ```

---

### **12. What is the `@SpyBean` annotation in Spring Boot?**
- **Purpose**: Adds a spy bean to the Spring application context.
- **Usage**: Used in tests to partially mock dependencies.
- **Example**:
  ```java
  @SpringBootTest
  public class MyTest {
      @SpyBean
      private MyService myService;
  }
  ```

---

### **13. What is the `@WebMvcTest` annotation in Spring Boot?**
- **Purpose**: Used for testing Spring MVC controllers.
- **Usage**: Configures only the web layer for testing.
- **Example**:
  ```java
  @WebMvcTest(UserController.class)
  public class UserControllerTest {
      // Test methods
  }
  ```

---

### **14. What is the `@DataJpaTest` annotation in Spring Boot?**
- **Purpose**: Used for testing JPA repositories.
- **Usage**: Configures only the data layer for testing.
- **Example**:
  ```java
  @DataJpaTest
  public class UserRepositoryTest {
      // Test methods
  }
  ```

---

### **15. What is the `@RestClientTest` annotation in Spring Boot?**
- **Purpose**: Used for testing REST clients.
- **Usage**: Configures only the REST client for testing.
- **Example**:
  ```java
  @RestClientTest(MyRestClient.class)
  public class MyRestClientTest {
      // Test methods
  }
  ```

---

### **16. What is the `@JsonTest` annotation in Spring Boot?**
- **Purpose**: Used for testing JSON serialization and deserialization.
- **Usage**: Configures only the JSON-related components for testing.
- **Example**:
  ```java
  @JsonTest
  public class MyJsonTest {
      // Test methods
  }
  ```

---

### **17. What is the `@TestConfiguration` annotation in Spring Boot?**
- **Purpose**: Defines additional beans for testing.
- **Usage**: Used to provide test-specific configurations.
- **Example**:
  ```java
  @TestConfiguration
  public class TestConfig {
      @Bean
      public MyBean myBean() {
          return new MyBean();
      }
  }
  ```

---

### **18. What is the `@Conditional` annotation in Spring Boot?**
- **Purpose**: Conditionally registers a bean based on a specified condition.
- **Usage**: Used for conditional bean creation.
- **Example**:
  ```java
  @Bean
  @Conditional(MyCondition.class)
  public MyBean myBean() {
      return new MyBean();
  }
  ```

---

### **19. What is the `@ConditionalOnProperty` annotation in Spring Boot?**
- **Purpose**: Configures a bean based on the presence or value of a property.
- **Usage**: Used in auto-configuration classes.
- **Example**:
  ```java
  @Bean
  @ConditionalOnProperty(name = "feature.enabled", havingValue = "true")
  public MyBean myBean() {
      return new MyBean();
  }
  ```

---

### **20. What is the `@ConditionalOnExpression` annotation in Spring Boot?**
- **Purpose**: Configures a bean based on a SpEL expression.
- **Usage**: Used for complex conditional logic.
- **Example**:
  ```java
  @Bean
  @ConditionalOnExpression("${feature.enabled} && ${feature.mode} == 'advanced'")
  public MyBean myBean() {
      return new MyBean();
  }
  ```

---

### **21. What is the `@ConditionalOnMissingClass` annotation in Spring Boot?**
- **Purpose**: Configures a bean only if a specified class is **not** present in the classpath.
- **Usage**: Used in auto-configuration classes.
- **Example**:
  ```java
  @Bean
  @ConditionalOnMissingClass("com.example.OtherClass")
  public MyBean myBean() {
      return new MyBean();
  }
  ```

---

### **22. What is the `@ConditionalOnBean` annotation in Spring Boot?**
- **Purpose**: Configures a bean only if a specified bean is present in the application context.
- **Usage**: Used in auto-configuration classes.
- **Example**:
  ```java
  @Bean
  @ConditionalOnBean(DataSource.class)
  public MyBean myBean() {
      return new MyBean();
  }
  ```

---

### **23. What is the `@ConditionalOnMissingBean` annotation in Spring Boot?**
- **Purpose**: Configures a bean only if no bean of the specified type is already present in the application context.
- **Usage**: Used in auto-configuration classes.
- **Example**:
  ```java
  @Bean
  @ConditionalOnMissingBean
  public MyBean myBean() {
      return new MyBean();
  }
  ```

---

### **24. What is the `@ConditionalOnResource` annotation in Spring Boot?**
- **Purpose**: Configures a bean only if a specified resource is present.
- **Usage**: Used in auto-configuration classes.
- **Example**:
  ```java
  @Bean
  @ConditionalOnResource(resources = "classpath:config.properties")
  public MyBean myBean() {
      return new MyBean();
  }
  ```

---

### **25. What is the `@ConditionalOnWebApplication` annotation in Spring Boot?**
- **Purpose**: Configures a bean only if the application is a web application.
- **Usage**: Used in auto-configuration classes.
- **Example**:
  ```java
  @Bean
  @ConditionalOnWebApplication
  public MyBean myBean() {
      return new MyBean();
  }
  ```

---

### **26. What is the `@ConditionalOnNotWebApplication` annotation in Spring Boot?**
- **Purpose**: Configures a bean only if the application is **not** a web application.
- **Usage**: Used in auto-configuration classes.
- **Example**:
  ```java
  @Bean
  @ConditionalOnNotWebApplication
  public MyBean myBean() {
      return new MyBean();
  }
  ```

---

### **27. What is the `@ConditionalOnSingleCandidate` annotation in Spring Boot?**
- **Purpose**: Configures a bean only if a single candidate of the specified type is present in the application context.
- **Usage**: Used in auto-configuration classes.
- **Example**:
  ```java
  @Bean
  @ConditionalOnSingleCandidate(DataSource.class)
  public MyBean myBean() {
      return new MyBean();
  }
  ```

---

Let me know if you need further clarification! 😊