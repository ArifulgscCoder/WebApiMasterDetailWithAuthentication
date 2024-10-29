A Web API Master-Detail with Authentication for Product Management is an ASP.NET Core Web API project that enables secure CRUD operations on products with related details (such as product variations or inventory entries) while enforcing user authentication. This structure is ideal for an e-commerce or inventory management system where each product may have multiple details associated with it.

Key Features:
Authentication & Authorization:

User Registration: New users can register with email and password.
Login & Token-based Authentication: Users log in to receive a JWT token for secure access to API endpoints.
Role-based Authorization: Roles such as Admin and User restrict access to certain endpoints, like product management (Admin only).
Product Management (Master Entity):

CRUD operations for Product with fields like ProductID, ProductName, Category, Price, and Description.
Products act as the master entity and serve as the basis for related details.
Product Details Management (Detail Entity):

Example detail entities:
Product Variations: Variations of a product (e.g., different colors or sizes) with fields such as VariationID, Color, Size, and Stock.
Inventory Entries: Records of product stock, including fields like InventoryID, WarehouseLocation, Quantity, and DateReceived.
CRUD operations for each detail entity, linked to a specific product.
Endpoints:

Product Endpoints: /api/products for managing products (Admin only).
Detail Endpoints: /api/products/{productId}/variations or /api/products/{productId}/inventory for managing details associated with each product.
Authentication Endpoints: /api/auth/register, /api/auth/login to manage user authentication.
Security:

JWT (JSON Web Tokens): For secure, token-based authentication.
Authorization Attributes: Controllers and actions are secured based on user roles.
Entity Relationships:

Define relationships between Product (master) and details (Variations, InventoryEntries) using Entity Framework Core.
Tech Stack:
ASP.NET Core Web API: For building RESTful services and implementing authentication.
Entity Framework Core: For managing data and relationships in a relational database.
JWT Authentication: For secure access control with user roles.
SQL Database: For storing user, product, and related detail data.
Example Use Cases:
E-commerce Platform: Admins can manage products and related details like color or size options, while users can view the available options.
Inventory Management System: Track each product’s variations and stock details across multiple warehouses with authorized access only.
This project combines essential concepts in ASP.NET Core, such as master-detail relationships, JWT authentication, and role-based authorization, to provide a comprehensive foundation for a secure, scalable product management API.
