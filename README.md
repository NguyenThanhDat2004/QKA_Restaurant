# 🍽️ Restaurant QKA - Restaurant Management System

<div align="center">
  <img src="https://img.shields.io/badge/ASP.NET%20MVC-5.2.7-0062A8?style=for-the-badge&logo=.net" alt="ASP.NET MVC" />
  <img src="https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white" alt="C#" />
  <img src="https://img.shields.io/badge/.NET%20Framework-4.8-512BD4?style=for-the-badge&logo=.net" alt=".NET Framework 4.8" />
  <img src="https://img.shields.io/badge/Entity%20Framework-6-8A2BE2?style=for-the-badge" alt="Entity Framework 6" />
  <img src="https://img.shields.io/badge/SQL%20Server-CC2927?style=for-the-badge&logo=microsoft-sql-server&logoColor=white" alt="SQL Server" />
</div>

<p align="center">
  <strong>Restaurant QKA</strong> is a comprehensive restaurant management web application built with <b>ASP.NET MVC 5</b> and <b>Entity Framework 6</b>.  
  It supports multiple user roles and provides full control over menu, orders, employees, inventory, and suppliers.
</p>

---

## 📖 Table of Contents

* [✨ Key Features](#-key-features)
* [🏛️ Project Architecture](#️-project-architecture)
* [🛠️ Technologies Used](#️-technologies-used)
* [🚀 Getting Started](#-getting-started)

  * [📋 Requirements](#-requirements)
  * [⚙️ Installation Steps](#️-installation-steps)
* [🤝 Contributing](#-contributing)

---

## ✨ Key Features

A modular and fully-featured restaurant management system designed for real-world operations.

### 👥 Role-Based Access Control

The system separates functionalities using **ASP.NET MVC Areas**, providing isolated modules for each user role:

* **Admin** – Full control over system settings, employees, customers, menu, and discounts.
* **User (Customer)** – Browse the menu, place orders, manage the cart, and track order history.
* **StaffChef** – Manage dishes, recipes, and preparation details.
* **StaffOrder** – Handle and confirm customer orders.
* **StaffWareHouse** – Manage inventory, suppliers, and warehouse transactions.

### 🍴 Menu & Dish Management

Easily add, edit, delete, and categorize menu items dynamically.

### 🛒 Order & Cart System

Supports a full ordering flow: cart, discount code, and checkout.

### 👨‍💼 Employee & Customer Management

Track details, performance, and activities of both employees and customers.

### 📦 Inventory & Supplier Control

Handle warehouse input/output transactions and manage supplier relationships.

### 🤖 Smart Recommendation System

Implements the **Hill Climbing algorithm** to suggest dishes intelligently based on user preferences.

### 📊 Data Pagination

Uses **PagedList.Mvc** for efficient pagination and data rendering.

### 📧 Email Service

Includes an **EmailService** module to send automatic notifications such as order confirmations and password resets.

---

## 🏛️ Project Architecture

* **MVC Pattern (Model–View–Controller)**: Clean separation between business logic, UI, and control flow.
* **ASP.NET MVC Areas**: Modular structure for maintainability and scalability.
* **Entity Framework (Database First)**: Automatically generates models from an existing database (`Model1.edmx`).
* **Bundling & Minification**: Configured in `BundleConfig.cs` for optimized loading of CSS and JS files.

---

## 🛠️ Technologies Used

### 🔹 Backend

* **Language:** C#
* **Framework:** ASP.NET MVC 5, .NET Framework 4.8
* **ORM:** Entity Framework 6
* **Data Query:** LINQ

### 🔹 Frontend

* **Technologies:** HTML5, CSS3, JavaScript
* **Libraries:** jQuery, Bootstrap
* **Plugins:** Chart.js, DataTables, Bootstrap Datepicker, Select2

### 🔹 Database

* **Database System:** Microsoft SQL Server

### 🔹 Tools & Environment

* **IDE:** Visual Studio 2017 / 2019 / 2022
* **Package Manager:** NuGet

---

## 🚀 Getting Started

Follow the steps below to run this project locally.

### 📋 Requirements

* **Visual Studio** 2019 or 2022
* **.NET Framework 4.8 Developer Pack**
* **Microsoft SQL Server** (version 2012 or higher)

### ⚙️ Installation Steps

1. **Clone the repository**

   ```bash
   git clone https://github.com/YOUR_USERNAME/Restaurant_QKA.git
   cd Restaurant_QKA
   ```

2. **Open the project**

   * Launch `Restaurant_QKA.sln` in Visual Studio.

3. **Restore NuGet packages**
   Visual Studio will restore packages automatically on the first build.
   If not, open **Package Manager Console** and run:

   ```powershell
   Update-Package -reinstall
   ```

4. **Configure the connection string**

   * Open `Web.config`.
   * Locate the `<connectionStrings>` section and update your SQL instance:

     ```xml
     <add name="qka_restaurantEntities" 
          connectionString="metadata=res://*/Models.Model1.csdl|res://*/Models.Model1.ssdl|res://*/Models.Model1.msl;provider=System.Data.SqlClient;provider connection string=&quot;data source=YOUR_SERVER_NAME;initial catalog=YOUR_DATABASE_NAME;integrated security=True;MultipleActiveResultSets=True;App=EntityFramework&quot;" 
          providerName="System.Data.EntityClient" />
     ```

5. **Setup Database**

   * Import the provided `.sql` script into SQL Server to create tables and seed data.
   * Alternatively, generate the schema from `Model1.edmx`.

6. **Run the project**
   Press **F5** or click **Start** in Visual Studio to build and launch the app.

---

## 🤝 Contributing

Contributions are welcome! Follow the steps below to submit improvements.

1. Fork this repository
2. Create your feature branch

   ```bash
   git checkout -b feature/AmazingFeature
   ```
3. Commit your changes

   ```bash
   git commit -m "Add some AmazingFeature"
   ```
4. Push to the branch

   ```bash
   git push origin feature/AmazingFeature
   ```
5. Open a Pull Request

⭐ If you like this project, please give it a **star** to support development!
