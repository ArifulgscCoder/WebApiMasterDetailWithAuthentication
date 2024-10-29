# 🛠️ Web API Master-Detail with Authentication for Product Management

## 📜 Description
This project is an **ASP.NET Core Web API** designed to enable secure CRUD operations on products and their related details (such as product variations or inventory entries) while enforcing user authentication. This structure is ideal for e-commerce or inventory management systems where each product may have multiple details associated with it.

---

## 🚀 Key Features

### 🔒 Authentication & Authorization
- **User Registration**: New users can register with email and password.
- **Login & Token-based Authentication**: Users log in to receive a JWT token for secure access to API endpoints.
- **Role-based Authorization**: Roles such as Admin and User restrict access to certain endpoints, like product management (Admin only).

### 📦 Product Management (Master Entity)
- **CRUD Operations**: Manage products with fields like:
  - **ProductID**
  - **ProductName**
  - **Category**
  - **Price**
  - **Description**

### 📊 Product Details Management (Detail Entity)
- **Example Detail Entities**:
  - **Product Variations**: Variations of a product (e.g., different colors or sizes) with fields such as:
    - **VariationID**
    - **Color**
    - **Size**
    - **Stock**
  - **Inventory Entries**: Records of product stock, including fields like:
    - **InventoryID**
    - **WarehouseLocation**
    - **Quantity**
    - **DateReceived**

### 🛠️ Endpoints
- **Product Endpoints**: `POST /api/products` for managing products (Admin only).
- **Detail Endpoints**: 
  - `GET /api/products/{productId}/variations` for managing variations.
  - `GET /api/products/{productId}/inventory` for managing inventory entries.
- **Authentication Endpoints**: 
  - `POST /api/auth/register` for user registration.
  - `POST /api/auth/login` for user login.

### 🔐 Security
- **JWT (JSON Web Tokens)**: For secure, token-based authentication.
- **Authorization Attributes**: Controllers and actions secured based on user roles.

### 🏗️ Entity Relationships
- Define relationships between Product (master) and details (Variations, InventoryEntries) using **Entity Framework Core**.

---

## 🛠️ Tech Stack
- **ASP.NET Core Web API**: For building RESTful services and implementing authentication.
- **Entity Framework Core**: For managing data and relationships in a relational database.
- **JWT Authentication**: For secure access control with user roles.
- **SQL Database**: For storing user, product, and related detail data.

---

## 🌟 Example Use Cases
- **E-commerce Platform**: Admins can manage products and related details like color or size options, while users can view the available options.
- **Inventory Management System**: Track each product’s variations and stock details across multiple warehouses with authorized access only.

---

## 💻 Getting Started

### Prerequisites
- [.NET SDK 6.0 or later](https://dotnet.microsoft.com/download)
- [SQL Server Express](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)

### Installation Steps
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/product-management-api.git
   cd product-management-api
