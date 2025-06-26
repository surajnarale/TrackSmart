# ✅ TrackSmart 📊 – Smart Attendance Management API

**TrackSmart** is a powerful and flexible Spring Boot REST API designed to digitize and automate student attendance tracking for educational institutions.
It enables seamless operations for managing students, faculty, subjects, and attendance records, ensuring precision, efficiency, and modern workflow integration.

---

## 🚀 Key Highlights

- 🎯 End-to-end attendance lifecycle automation
- 🔐 Secure authentication with user registration & login
- 👨‍🏫 Faculty & subject data management
- 📅 Robust attendance tracking with history view
- 🏗️ Clean layered architecture with scalability in mind
- 🔌 Easily integrable with external educational platforms

---

## 🛠️ Tech Stack

| Layer        | Technology            |
|--------------|------------------------|
| Language     | Java (JDK 1.8)         |
| Backend      | Spring Boot 2.5.6      |
| ORM          | Hibernate (JPA 5.6)    |
| Database     | MySQL 8                |
| Build Tool   | Maven                  |
| IDE          | Eclipse                |
| API Testing  | Postman                |

---

## 🎯 Project Objective

- ✅ Eliminate manual attendance handling through digital automation
- ✅ Ensure data integrity with validations and structured storage
- ✅ Enhance productivity for faculty and admin teams
- ✅ Enable rapid integration with modern LMS platforms

---

## 🧱 Project Structure

com.tracksmart
├── controller # Handles HTTP requests (API layer)
├── service # Core business logic layer
├── dao # Data persistence layer (JPA repositories)
├── entity # POJOs representing DB tables
├── dto # Data Transfer Objects (if used)
└── exception # Centralized exception handling




## 📚 API Modules & Endpoints

### 👨‍🎓 Student APIs

| Method | Endpoint                                | Description                      |
|--------|-----------------------------------------|----------------------------------|
| GET    | `/student/get-all-students`             | Retrieve all student records     |
| POST   | `/student/add-student`                  | Add a new student                |
| GET    | `/student/get-student-by-id/{id}`       | Get student by ID                |
| PUT    | `/student/update-student`               | Update student information       |
| DELETE | `/student/delete-student/{id}`          | Delete a student record          |

---

### 📘 Subject APIs

| Method | Endpoint                                | Description                       |
|--------|-----------------------------------------|-----------------------------------|
| GET    | `/subject/get-all-subjects`             | Retrieve all subjects             |
| POST   | `/subject/add-subject`                  | Create a new subject              |
| GET    | `/subject/get-subject-by-id/{id}`       | Get subject details by ID         |
| PUT    | `/subject/update-subject`               | Update subject information        |
| DELETE | `/subject/delete-subject/{id}`          | Remove a subject from the system  |

---

### 👨‍🏫 Faculty APIs

| Method | Endpoint                                | Description                       |
|--------|-----------------------------------------|-----------------------------------|
| GET    | `/faculty/get-all-faculties`            | View all faculty records          |
| POST   | `/faculty/add-faculty`                  | Add a new faculty member          |
| GET    | `/faculty/get-faculty-by-id/{id}`       | View faculty by ID                |
| PUT    | `/faculty/update-faculty`               | Modify faculty information        |
| DELETE | `/faculty/delete-faculty/{id}`          | Delete a faculty record           |

---

### 🗓️ Attendance APIs

| Method | Endpoint                                     | Description                          |
|--------|----------------------------------------------|--------------------------------------|
| GET    | `/attendance/get-all-attendance-records`     | Retrieve all attendance entries      |
| POST   | `/attendance/add-attendance`                 | Add new attendance record            |

> 📌 When recording attendance:
> - Provide **Subject ID**
> - Provide **List of Student IDs**
> - Provide **Date**
> - Provide **Faculty ID** (as attendance taker)

---

### 👤 User APIs

| Method | Endpoint                                 | Description                          |
|--------|------------------------------------------|--------------------------------------|
| POST   | `/user/login-user`                       | Authenticate a user                  |
| POST   | `/user/register-user`                    | Register a new user                  |
| GET    | `/get-user-by-username/{username}`       | Fetch user details by username       |
| GET    | `/get-all-user`                          | List all registered users            |
| DELETE | `/get-all-user?username={username}`      | Delete user by username              |

---

## 🧬 ER Diagram & Database Design

- **Entities**: `Student`, `Subject`, `Faculty`, `Attendance`, `User`
- **Relationships**:
  - `Attendance` ⬌ `Student` : Many-to-Many
  - `Attendance` ⬌ `Faculty` : Many-to-One
  - `Attendance` ⬌ `Subject` : Many-to-One



---

## ⚙️ Getting Started

1️⃣ **Clone the repository**

```bash
git clone https://github.com/your-username/TrackSmart.git
cd TrackSmart
2️⃣ Configure MySQL

Update your application.properties file with the correct database credentials:

properties
Copy
Edit
spring.datasource.url=jdbc:mysql://localhost:3306/tracksmart_db
spring.datasource.username=root
spring.datasource.password=your_password
3️⃣ Run the application

bash
Copy
Edit
mvn spring-boot:run
4️⃣ Test with Postman

Use the above endpoints to interact with the system.

🧪 Sample JSON Payloads
➕ Insert Student
json
Copy
Edit
{
  "name": "Suraj Narale",
  "email": "suraj@example.com",
  "mobileNumber": "9876543210",
  "address": "Kurvenagar, Mumbai"
}
📝 Register New User
json
Copy
Edit
{
  "username": "surajnarale",
  "email": "surajnarale@example.com",
  "password": "securePass123"
}

👤 Author
Suraj Hanmant Narale
📍 Pune, Maharashtra
📧 Email: surajnarale5152@gmail.com
📱 Mobile: +91-8767198133
💼 Full Stack Java Developer | REST API Enthusiast

🌟 Show Your Support
If you found this project helpful, consider giving it a ⭐ star on GitHub!
