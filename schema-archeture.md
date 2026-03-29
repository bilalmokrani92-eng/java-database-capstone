This Spring Boot application uses both MVC and REST controllers. Thymeleaf templates are used for the Administrator and Doctor dashboards, while REST APIs serve all other modules. The application interacts with two databases: MySQL (for patient, doctor, appointment, and administrator data) and MongoDB (for prescriptions). All controllers route requests through a common service layer, which in turn delegates to the appropriate repositories. MySQL uses JPA entitie and MongoDB uses document models.
1. User accesses AdminDashboard or Appointment pages.
2. The action is routed to the appropriate Thymeleaf or REST controller.
The controller calls the service layer to process the request.
3. The service layer applies business logic and validations.
The service interacts with the repository layer to access data.
4. The repository communicates with MySQL or MongoDB databases.
5. Data is retrieved and mapped into model objects (entities or documents).
6. The service returns processed data back to the controller.
7. The controller prepares the response:
HTML view via Thymeleaf (MVC)
JSON response via REST API
The response is sent back to the user (browser or API client).