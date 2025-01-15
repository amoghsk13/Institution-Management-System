# Institution-Management-System
**This project consists of three components:**

1. **Eureka Server**
2. **Gateway Service**
3. **Student Service**
4. **Teacher Service**
5. **School Service**

**Prerequisites:**
- Java Development Kit (JDK)
- Maven
- Postman (for testing)
- IDE (e.g., IntelliJ IDEA, Eclipse)

**Instructions:**
1. Start the Eureka application: `EurekaApplication` in the Eureka Server project.
2. Start the Gateway service: `GatewayServiceApplication` in the Gateway Service project.
3. Start the Student service: `StudentServiceApplication` in the Student Service project.
4. Start the Teacher service: `TeacherServiceApplication` in the Teacher Service project.
5. Start the School service: `SchoolServiceApplication` in the School Service project.
6. Test the APIs using Postman as demonstrated in the project.

**Project Flow and Communication:**

**Flow of the Project:**
- **Eureka Server:**
  - Acts as the service registry for all microservices.
  - All services (Student, Teacher, School) register themselves with the Eureka Server for service discovery.

- **Gateway Service:**
  - Serves as a single entry point for all client requests.
  - Routes requests to the appropriate microservices based on the URI.

- **Student Service:**
  - Manages operations related to students, such as creating, retrieving, updating, and deleting student records.
  - Registers with the Eureka Server for service discovery.

- **Teacher Service:**
  - Manages operations related to teachers, including adding, retrieving, updating, and deleting teacher records.
  - Also registers with the Eureka Server.

- **School Service:**
  - Handles operations related to schools, such as adding, retrieving, updating, and deleting school records.
  - Registers with the Eureka Server.

**Role of Eureka and Gateway:**
- **Eureka:**
  - Provides service discovery, allowing all services to dynamically discover and communicate with each other without hardcoded URLs.
  - Each service registers itself with Eureka and retrieves service instances from the registry.

- **Gateway:**
  - Simplifies client interactions by routing requests to the appropriate service based on the request URI.
  - Acts as a reverse proxy, forwarding requests to the respective microservices.

By combining Eureka and the Gateway service, the system ensures scalability, flexibility, and ease of communication between microservices, allowing for efficient management of student, teacher, and school data. 

**Testing:**
- The APIs for all services can be tested through the Gateway using Postman, including creating, retrieving, updating, and deleting records for schools, teachers, and students. 

**Conclusion:**
- This architecture promotes a microservices approach, enhancing modularity and maintainability of the application.
