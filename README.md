# TeamSync
Made with 💖 by Joel Jolly.

# About
TeamSync is a comprehensive employee management and project tracking application designed to streamline the way you manage your workforce and projects. With TeamSync, you can effortlessly keep track of employee details, monitor the status of ongoing projects, and manage department information, all from a unified platform.

# Project Current Progress
1. Install Required Tools: ✅ 
2. Create a New Spring Boot Project: ✅ 
3. Set Up Version Control: ✅ 
4. Design the Database Schema: ✅ 
5. Configure MySQL Connection: ✅ 
6. Create JPA Entities: ✅ 
7. Create Repository Interfaces: ✅ 
8. Implement the Service Layer: ✅ 
9. Create REST Controllers: ✅ 
10. Handle Validation: ✅ 
11. Test with Postman: ❌ (Have conducted few tests) (None shown any progress)
12. Write Unit and Integration Tests: ✅ 
13. Implement Basic Security (Optional): ✅
  * (Secured in the HTML level)
15. Prepare Documentation: ✅ (Almost)
16. Deploy the Application: ❌ (Tried, but failed multiple times) (Working on it)
17. Code Review and Feedback: Pending

# To get started
* Create a database
```
CREATE DATABASE teamsync;
```
* Enter inside the database
```
USE teamsync_db;
```

* Create a table called `department`

```
CREATE TABLE department (
  id BIGINT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(100) NOT NULL
);
```

* Create a table called `employee`
```
CREATE TABLE employee (
  id BIGINT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(100) NOT NULL,
  email VARCHAR(100) NOT NULL,
  department_id BIGINT,
  FOREIGN KEY (department_id) REFERENCES department(id)
);
```
* Create a table called `project`
```
CREATE TABLE project (
  id BIGINT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(100) NOT NULL,
  description TEXT,
  employee_id BIGINT,
  FOREIGN KEY (employee_id) REFERENCES employee(id)
);
```
* Update the `application.properties`
```
spring.application.name=teamsync
spring.datasource.url=jdbc:mysql://localhost:3306/teamsync  //replace teamsync with your database name.
spring.datasource.username=root  //mysql name
spring.datasource.password=test123!  //mysql password
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```
* Paste the repo code inside the intellij project folder. (Before doing this create a new project using intellij and then close the intellij app and then paste the code from this repo)
* Run the `build.gradle` (To install the packages)
* Run the code.

# Support Me
If you love Elsa and want to keep me caffeinated for more awesome updates, consider buying me a coffee!

[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Donate-orange?style=for-the-badge&logo=buy-me-a-coffee)](https://www.buymeacoffee.com/withinjoel)

Made with 💖 by Joel Jolly.
