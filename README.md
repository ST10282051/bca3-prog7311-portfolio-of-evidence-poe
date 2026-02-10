# AgriEnergyConnect_ST10282051

AgriEnergyConnect is a role-based agricultural web platform that connects farmers, employees, and administrators. It allows farmers to manage their products, employees to assist with product oversight, and all users to engage in a community-driven news feed.

## Table of Contents

1. [About the Project](#about-the-project)  
2. [System Functionalities](#system-functionalities)  
3. [User Roles](#user-roles)  
4. [User Interface & Design](#user-interface--design)  
5. [Setup Instructions](#setup-instructions)  
6. [Build & Run the Project](#build--run-the-project)  
7. [Project Structure](#project-structure)  
8. [Technologies Used](#technologies-used)  

## About the Project

AgriEnergyConnect is designed to streamline communication and productivity in the agricultural sector. It allows:

- **Farmers** to manage their products.
- **Employees** to oversee farmers and their inventories.
- **Administrators** to manage the system.
- **All users** to post content in a shared news feed.

## System Functionalities

### For Farmers
- Add new products with:
  - Name, category, production date, and image
- View and manage their own products

### For Employees
- Add farmer profiles with personal details
- View products from any farmer
- Filter products by:
  - Date range
  - Category/type

### For All Users(Farmers and Employees)
- View and post to the news feed
- Comment on community posts
- Community can view post but not comment

## User Roles

Role       Description
Farmer     Can add/view products, and participate in news feed                         
Employee   Can manage farmer profiles, view all farmer products, and filter by criteria
Admin      Has full access to dashboards and user management                           
Guest      Can view public pages only                                                  

## User Interface & Design

- **Responsive Design**: Mobile, tablet, and desktop compatible
- **Intuitive Navigation**: Clear layout and structured menus
- **Accessible UI**: Simple and inclusive design for all user types
- **Error Handling**: Friendly messages and fallback pages

## Setup Instructions
Follow these steps to set up the development environment on your local machine.

### 1. Requirements
.NET 6 SDK or newer
Visual Studio 2022+ (with ASP.NET workload)
SQL Server Express or LocalDB
Git (optional)


### 2. Clone the Project
https://github.com/VCPTA/bca3-prog7311-portfolio-of-evidence-poe-ST10282051.git

## Database Setup (SSMS + EF Core Migrations)
Follow these quick steps to connect your project to SQL Server and run migrations.

### Requirements
- SQL Server Express or LocalDB
- SQL Server Management Studio (SSMS)
- .NET 6 SDK+
- Visual Studio 2022+

### Steps
#### 1. Create the Database in SSMS
Open SSMS and connect to your local SQL Server instance
Right-click Databases > New Database...
Name the database: AgriEnergyConnectDB

#### 2. Update the Connection String
In appsettings.json: {
  "ConnectionStrings": {
    "DefaultConnection": "Data Source=lab7L95SR\\SQLEXPRESS;Initial Catalog=ST10282051AgriConnect;Integrated Security=True;Connect Timeout=30;Encrypt=True;Trust Server Certificate=True;Application Intent=ReadWrite;Multi Subnet Failover=False"
  },
  "Logging": {
    "LogLevel": {
      "Default": "Information",
      "Microsoft.AspNetCore": "Warning"
    }
  },
  "AllowedHosts": "*"
}

#### 3. Apply Migrations
Open Visual Studio
Go to Tools > NuGet Package Manager > Package Manager Console
Set the default project to the one containing your DbContext
Run: Add-Migration First
Update-Database

#### 4. Confirm in SSMS
Refresh the database to see the created tables and data.

#### 5. Run the Project
Press F5 in Visual Studio to build and launch the web application.

## Project Structure
Controllers – Handle incoming requests
Views – User-facing pages (Razor Views)
Models – Represent database entities
Data – Contains DbContext and migrations

## Technologies Used
- ASP.NET Core MVC
- Entity Framework Core
- SQL Server
- Visual Studio
- Git & GitHub




