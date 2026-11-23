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

## How to Run
1. Clone the repository:
   ```bash
   git clone [https://github.com/s3eedbaz/ContosoUniversity.git](https://github.com/s3eedbaz/ContosoUniversity.git)
   cd ContosoUniversity