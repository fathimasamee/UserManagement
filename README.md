
Simple User Management CRUD - ASP.NET Core MVC

A basic user management web application using ASP.NET Core MVC and Entity Framework Core. It provides full CRUD (Create, Read, Update, Delete) functionality for managing users.



✅ .NET Version Used

*  .NET 8 



Setup and Run Instructions

1. Clone or Download the Repository

   
   git clone https://github.com/fathimasamee/UserManagement.git
   cd UserManagement
   

2. Open the Project

   Open the project in Visual Studio 2022 or later.

3. Install Required NuGet Packages

   Open the Package Manager Console and run.


   Install-Package Microsoft.EntityFrameworkCore.SqlServer
   Install-Package Microsoft.EntityFrameworkCore.Tools


4. Configure the Database Connection

   In `appsettings.json`, ensure your connection string is correct.


   "ConnectionStrings": {
     "DefaultConnection": "Server=(localdb)\\Local;Database=UserManagementDB1;Trusted_Connection=true"
   }


5. Apply Migrations and Create the Database

   In Package Manager Console, run

   Add-Migration InitialCreate
   Update-Database


6. (Optional) Add Sample Data

   Use SQL script (in README or seed via `OnModelCreating` in `UserContext.cs`) to add users:


   INSERT INTO Users (Username, Password, Role) VALUES 
   ('admin', 'admin123', 'Admin'),
   ('john', 'john123', 'Staff'),
   ('mary', 'mary123', 'Staff');


7. Run the Application

   Press F5 or click Run



Assumptions and Notes

* No authentication or authorization is implemented—this project focuses on CRUD operations only.
* Passwords are stored in plain text. this is NOT secure and intended for demonstration only.In real applications, always hash passwords.
* Simple MVC structure using Entity Framework Core for data access.


