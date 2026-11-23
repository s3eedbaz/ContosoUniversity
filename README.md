# Contoso University - ASP.NET Core MVC with EF Core

An ASP.NET Core MVC web application implementing database initialization and basic CRUD operations (Create, Read, Update, Delete) for managing students and course enrollments using Entity Framework Core and SQL Server LocalDB.

## Author
- **Name:** Saeed Mohammed Bazmool (سعيد محمد بازمول)
- **Institution:** Hadhramout University - Computer Engineering
- **GitHub:** [@s3eedbaz](https://github.com/s3eedbaz)

## Technologies Used
- **.NET 11** (`net11.0`) / **ASP.NET Core MVC**
- **Entity Framework Core** (`Microsoft.EntityFrameworkCore.SqlServer`)
- **SQL Server LocalDB** (`ContosoUniversity1`)
- **Bootstrap 5** & **Razor Views**

## Implemented Features
1. **Database Initialization & Seeding (`DbInitializer`):**
   - Automatically creates and seeds `Student`, `Course`, and `Enrollment` tables on startup using `EnsureCreated()`.
   - Configured EF Core SQL command logging in `appsettings.Development.json`.
2. **Student CRUD Operations (`StudentsController`):**
   - **Index:** Displays the full list of students.
   - **Details:** Uses eager loading (`Include`, `ThenInclude`) and `AsNoTracking()` to display student details along with enrolled courses and grades.
   - **Create:** Protected against overposting using `[Bind]` and server-side `ModelState` validation.
   - **Edit:** Uses the read-first pattern with `TryUpdateModelAsync` to prevent overposting and update only modified columns.
   - **Delete:** Confirmation view with `DbUpdateException` error handling.
## Screenshots

### 1. Students List (Index)
<!--  -->
<img width="1366" height="681" alt="contoso1" src="https://github.com/user-attachments/assets/be9a3e6d-0f2e-4501-a556-659f0460906b" />

### 2. Student Details & Enrollments
 <img width="1366" height="690" alt="contosodetails" src="https://github.com/user-attachments/assets/acb86017-1011-48c3-9dff-75a7c542d9c2" />
 -->

### 3. Create New Student
 <img width="1366" height="683" alt="contosocreate" src="https://github.com/user-attachments/assets/a98b820e-a589-4608-885f-211fd1211030" />
-->

### 4. Edit Student
 <img width="1358" height="689" alt="contosoEdit" src="https://github.com/user-attachments/assets/6085e976-859d-4df6-ba62-28f5aa7a4d68" />
-->

### 5. Delete Student
 <img width="1366" height="681" alt="contosodelete" src="https://github.com/user-attachments/assets/677aa779-c6ca-4aa3-9357-c5fee467330f" />
-->
## How to Run
1. Clone the repository:
   ```bash
   git clone [https://github.com/s3eedbaz/ContosoUniversity.git](https://github.com/s3eedbaz/ContosoUniversity.git)
   cd ContosoUniversity
