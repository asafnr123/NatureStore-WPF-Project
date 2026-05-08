# 🌿 NatureStore — WPF Desktop Application

A Windows desktop application simulating a **nutrition supplement store**, built with **C# and WPF** following a clean **MVC (Model-View-Controller)** architecture. Users can browse products, place orders, and manage their account — while admins have full control over the store.

---

## 📋 Table of Contents

- [About](#about)
- [Features](#features)
- [Architecture](#architecture)
- [Project Structure](#project-structure)
- [Tech Stack](#tech-stack)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [First Run](#first-run)
- [Login Credentials](#login-credentials)

---

## About

NatureStore simulates an online nutrition store selling products such as **protein powders, protein bars, vitamins, and more**. The application supports two types of users — regular customers and administrators — each with a dedicated interface and feature set.

> ⚠️ Note: The application does not include a payment system. Orders are managed without financial transactions.

---

## Features

### 👤 User Management
- User registration with full validation:
  - Checks if a username already exists
  - Enforces minimum password length and complexity
  - Validates all additional user details on sign-up
- Two login modes: **Regular User** and **Admin**

### 🛒 Regular User
- Browse available products by category
- Place orders for products
- View personal order history
- View and manage account details

### 🛠️ Admin
- View **all orders** across all users
- Add new products (with image validation — checks if the image path exists on disk)
- Add new users, including additional admin accounts
- Full product management with validation:
  - Verifies products exist in the database before editing or deleting
  - Displays descriptive error messages when operations fail

---

## Architecture

The solution follows the **MVC pattern**, cleanly separated into three C# projects:

| Layer | Project | Responsibility |
|---|---|---|
| **Model** | `NatureStore.Model` | Entities, database access, and business rules |
| **Controller** | `NatureStore.Controller` | Application logic coordinating Model and View |
| **View** | `NatureStore.View` | WPF UI — windows, pages, and XAML layouts |

---

## Project Structure

```
NatureStore-WPF-Project/
├── NatureStore.sln
├── NatureStore.Model/          # Data layer
├── NatureStore.Controller/     # Business logic layer
└── NatureStore.View/           # WPF UI (startup project)
```

---

## Tech Stack

| Technology | Details |
|---|---|
| Language | C# (.NET) |
| UI Framework | WPF (Windows Presentation Foundation) |
| Database | SQL Server (local) |
| IDE | Visual Studio 2022 |
| Architecture | MVC (Model-View-Controller) |
| Platform | Windows |

---

## Prerequisites

- **Windows** operating system
- **Visual Studio 2022** with the **.NET desktop development** workload
- **SQL Server Management Studio (SSMS)** — required to host the database locally

---

## Getting Started

1. **Clone the repository**

   ```bash
   git clone https://github.com/asafnr123/NatureStore-WPF-Project.git
   cd NatureStore-WPF-Project
   ```

2. **Open the solution**

   Double-click `NatureStore.sln`, or open it via **File → Open → Project/Solution** in Visual Studio.

3. **Set the Startup Project**

   Right-click **`NatureStore.View`** in the Solution Explorer → **Set as Startup Project**.

4. **Run the application**

   Press **F5** to build and launch.

---

## First Run

On the **first launch**, the application will automatically:

- Create a **local SQL Server database** on your machine
- Set up all required tables
- Seed the database with an initial set of **products and categories**

This means you can start browsing and ordering products right away, without manually inserting any data.

---

## Login Credentials

### 🔑 Admin Account (pre-seeded)

| Field | Value |
|---|---|
| Username | `admin` |
| Password | `Admin1213!` |

Logging in as admin takes you to the **Admin Dashboard**, where you can manage products, users, and view all orders.

### 🙋 Regular User

You must **register a new account** before logging in as a regular user. Once registered, you'll have access to the store, product catalog, and your personal order history.

---

## Author

**Asaf** — [@asafnr123](https://github.com/asafnr123)
