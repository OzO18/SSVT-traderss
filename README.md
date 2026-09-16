# 📦 StockLive — SSVT Traders

## Smart Distribution Inventory, Retailer Billing & Sales Management System

**StockLive** is a web-based distribution management application developed for **SSVT Traders**.

The system is designed to support distributors and sales officers during retailer visits by providing a centralized interface for viewing product stock, managing retailer shops, creating bills, and monitoring sales performance.

The primary objective of StockLive is to make the distribution workflow **faster, more organized, and easier to monitor**.

---

# 📌 Table of Contents

1. [Project Overview](#-project-overview)
2. [Project Objective](#-project-objective)
3. [Problem Statement](#-problem-statement)
4. [Proposed Solution](#-proposed-solution)
5. [Project Features](#-project-features)
6. [System Modules](#-system-modules)
7. [User Authentication](#-1-user-authentication)
8. [Dashboard](#-2-dashboard)
9. [Inventory Management](#-3-inventory-management)
10. [Brands & Products](#-4-brands--products)
11. [Retailer Shop Management](#-5-retailer-shop-management)
12. [Retailer Billing](#-6-retailer-billing)
13. [Automatic Stock Depletion](#-7-automatic-stock-depletion)
14. [Sales Analytics](#-8-sales-analytics)
15. [Data Storage](#-data-storage)
16. [Stock Status Logic](#-stock-status-logic)
17. [Application Workflow](#-application-workflow)
18. [Technology Stack](#-technology-stack)
19. [Project Structure](#-project-structure)
20. [Product Catalog](#-product-catalog)
21. [Retailer Data](#-retailer-data)
22. [How to Run](#-how-to-run)
23. [How to Use](#-how-to-use)
24. [Security Features](#-security-features)
25. [Responsive Design](#-responsive-design)
26. [Business Benefits](#-business-benefits)
27. [Current Limitations](#-current-limitations)
28. [Future Enhancements](#-future-enhancements)
29. [Testing](#-testing)
30. [Use Cases](#-use-cases)
31. [Project Outcome](#-project-outcome)
32. [Conclusion](#-conclusion)

---

# 📖 Project Overview

Distribution companies handle multiple products, brands, retailers, orders, and sales transactions every day.

A sales officer visiting a retailer needs to know:

* Which products are available?
* How many units are available?
* Which products have low stock?
* Which products are unavailable?
* Which retailer is placing the order?
* What quantity should be billed?
* What is the total bill amount?
* How much stock remains after the sale?
* How many orders have been completed?
* What is the total revenue?

StockLive brings these operations into a single web-based system.

The application provides a dashboard containing:

```text
Login
   ↓
Dashboard
   ↓
Inventory
   ↓
Brands & Products
   ↓
Retailer Shops
   ↓
Retailer Billing
   ↓
Automatic Stock Depletion
   ↓
Sales Analytics
```

The application currently includes products from **Colgate, Godrej, and Kellogg's**.

---

# 🎯 Project Objective

The main objectives of StockLive are:

### 1. Improve Stock Visibility

Provide a clear view of available distributor inventory.

### 2. Simplify Retailer Billing

Allow sales officers to select a retailer, choose products, enter quantities, and complete a sale.

### 3. Reduce Manual Stock Calculation

Automatically deduct sold quantities from available inventory.

### 4. Manage Retailer Information

Maintain a list of retailer shops and their order counts.

### 5. Monitor Sales

Calculate revenue, number of orders, and average order value.

### 6. Provide a User-Friendly Interface

Create a simple dashboard that can be used from desktop and mobile screens.

---

# ❗ Problem Statement

Traditional distribution workflows can involve manual processes for checking stock and preparing retailer orders.

This can create difficulties such as:

* Manual stock checking
* Delayed billing
* Incorrect stock calculations
* Difficulty identifying low-stock products
* Difficulty maintaining retailer information
* Difficulty tracking completed sales
* Lack of a centralized dashboard

### Problem Scenario

A sales officer visits a retailer.

The retailer requests several products.

The sales officer needs to determine:

```text
Product → Available Stock → Required Quantity → Bill Amount
```

If this process is handled manually, it can take additional time and may result in errors.

StockLive provides a digital workflow to simplify this process.

---

# 💡 Proposed Solution

StockLive provides a centralized web application where the user can:

```text
Login
  ↓
View Dashboard
  ↓
Check Inventory
  ↓
Select Retailer
  ↓
Select Products
  ↓
Enter Quantity
  ↓
Generate Bill
  ↓
Complete Sale
  ↓
Automatically Reduce Stock
  ↓
Record Invoice
  ↓
Update Sales Analytics
```

The billing module specifically checks product availability before adding requested quantities to the bill.

---

# ✨ Project Features

## 🔐 Authentication

* User registration
* Gmail validation
* Password creation
* Password confirmation
* Duplicate account checking
* Login validation
* Session management
* Logout functionality

## 📊 Dashboard

* Total products
* Total stock units
* Low-stock count
* Out-of-stock count
* Inventory overview
* Quick actions
* Refresh functionality

## 📦 Inventory

* Product listing
* Product category
* Brand
* Price
* Stock quantity
* Stock status
* Product search

## 🏷️ Brands

* Colgate
* Godrej
* Kellogg's
* Product counts
* Complete product catalog

## 🏪 Retailers

* Add retailer shop
* Store location
* Contact number
* Order count

## 🧾 Billing

* Select retailer
* Select product
* Enter quantity
* Add products
* Remove products
* Calculate total
* Complete sale

## 📈 Sales Analytics

* Total revenue
* Total orders
* Average order value
* Recent invoices

---

# 🧩 System Modules

StockLive is divided into six primary application modules:

```text
┌───────────────────────────────┐
│       STOCKLIVE SYSTEM        │
└───────────────┬───────────────┘
                │
 ┌──────────────┼───────────────┐
 │              │               │
 ▼              ▼               ▼
LOGIN       DASHBOARD       INVENTORY
 │              │               │
 └──────────────┼───────────────┘
                │
        ┌───────┴────────┐
        ▼                ▼
     BRANDS           SHOPS
        │                │
        └───────┬────────┘
                ▼
             BILLING
                │
                ▼
        STOCK DEPLETION
                │
                ▼
        SALES ANALYTICS
```

The sidebar navigation in the application exposes Dashboard, Inventory, Brands & Products, Retailer Billing, Shops, and Sales Analytics.

---

# 🔐 1. User Authentication

## Registration

A new user can create an account using:

* Full Name
* Gmail Address
* Password
* Confirm Password

The system validates that the email follows a Gmail format and requires a minimum six-character password.

### Registration Process

```text
Enter Name
     ↓
Enter Gmail
     ↓
Enter Password
     ↓
Confirm Password
     ↓
Validate Details
     ↓
Create Account
     ↓
Store Account
```

The application prevents creating another account using an existing email address.

---

# 🔑 Login

The user logs in using:

```text
Gmail Address
+
Password
```

The system searches the stored accounts for matching credentials.

If valid:

```text
Login
 ↓
Create Session
 ↓
Open Dashboard
```

If invalid:

```text
Login
 ↓
Invalid Credentials
 ↓
Display Error
```

The application stores the login state using `sessionStorage`.

---

# 📊 2. Dashboard

The Dashboard is the main control center of StockLive.

It displays four important statistics:

### Total Products

Number of active product SKUs.

### Stock Units

Total quantity of all products currently available.

### Low Stock

Number of products whose stock is greater than zero but below the low-stock threshold.

### Out of Stock

Number of products whose stock is zero or below.

These values are calculated dynamically from the product inventory.

---

## Dashboard Inventory Overview

The dashboard also displays a summarized inventory table containing:

```text
Product
Brand
Stock
Status
```

The dashboard shows up to the first six products in this overview.

---

# ⚡ Quick Actions

The dashboard provides quick access to common operations:

* Create Retailer Bill
* Add Product
* Add Retailer Shop

This reduces the number of navigation steps required for common tasks.

---

# 📦 3. Inventory Management

The Inventory module provides a detailed product table.

Each product contains:

```text
Product Name
Category
Brand
Price
Stock
Status
```

The product inventory table is dynamically generated using JavaScript.

---

## 🔎 Product Search

The Inventory module contains a search box.

Users can type a product name, category, brand, or other visible table information.

Rows that do not match the entered search text are hidden.

---

# ➕ Add Product

New products can be added using the **Add Product** option.

The application asks for:

1. Product name
2. Brand
3. Category
4. Price
5. Stock quantity

The system validates price and stock values before adding the product.

---

# 🏷️ 4. Brands & Products

The Brands & Products module organizes the catalog by manufacturer.

## Supported Brands

### Colgate

**Category:** Oral Care Products

Products currently include:

* Colgate Salt 100g
* Colgate SF 9+3

### Godrej

**Category:** Home & Personal Care

Products currently include:

* Godrej Fab
* Cinthol Health+
* Cinthol Lime

### Kellogg's

**Category:** Packaged Food

Products currently include:

* Kellogg's Chocos
* Kellogg's Corn Flakes

The application dynamically calculates the number of products associated with each brand.

---

# 🏪 5. Retailer Shop Management

Retailers are managed through the Shops module.

Each retailer contains:

```text
Shop Name
Location
Contact
Orders
```

The application initially includes:

```text
Sri Murugan Stores — Madurai
SS Super Market — Coimbatore
```

---

# ➕ Adding a Retailer

The user can add a new retailer by entering:

```text
Shop Name
Location
Contact Number
```

The new retailer is added to the shops array and saved in browser storage.

---

# 🧾 6. Retailer Billing

Retailer Billing is one of the main operational modules.

The user selects:

### Step 1 — Retailer

Choose a shop from the retailer list.

### Step 2 — Product

Select an available product.

### Step 3 — Quantity

Enter the required quantity.

### Step 4 — Add Product

The product is added to the current bill.

### Step 5 — Review

The system calculates the subtotal and total amount.

### Step 6 — Complete Sale

The transaction is completed and inventory is updated.

The billing interface contains retailer selection, product selection, quantity entry, current bill display, total calculation, and Complete Sale functionality.

---

# 🧮 Bill Calculation

For each product:

```text
Subtotal = Product Price × Quantity
```

For multiple products:

```text
Total = Subtotal₁ + Subtotal₂ + ... + Subtotalₙ
```

Example:

```text
Product A
₹100 × 2 = ₹200

Product B
₹50 × 3 = ₹150

----------------
Total = ₹350
```

The application calculates each product subtotal and adds it to the overall bill total.

---

# 🚨 Stock Validation

Before adding a product to a bill, the application checks the available stock.

For example:

```text
Available Stock = 20
Requested Quantity = 25
```

The system rejects the request because the requested quantity exceeds available stock.

This validation is implemented in the `addToBill()` function.

---

# 🗑️ Remove Product From Bill

A product added to the current bill can be removed before completing the sale.

The application removes the selected product from the temporary bill and recalculates the displayed bill.

---

# 🔄 7. Automatic Stock Depletion

One of the important features of StockLive is automatic stock reduction after a completed sale.

Suppose:

```text
Product Stock = 100
Sold Quantity = 15
```

After completing the sale:

```text
Remaining Stock = 100 - 15
                = 85
```

The application performs this operation when `completeSale()` is executed.

---

# 🧾 Invoice Generation

After a successful sale, the application creates an invoice record containing:

```text
Invoice ID
Retailer Shop
Amount
Date
```

An invoice ID is generated using the current timestamp.

The completed sale is then added to the sales records.

---

# 📈 8. Sales Analytics

The Sales Analytics module summarizes completed transactions.

## Total Revenue

Calculated by adding the amount of all recorded sales.

```text
Total Revenue =
Sale 1 + Sale 2 + Sale 3 + ...
```

## Total Orders

The total number of recorded sales.

## Average Order Value

Calculated as:

```text
Average Order Value =
Total Revenue / Total Orders
```

The implementation calculates these values dynamically from the sales array.

---

# 🧾 Recent Invoices

The Sales Analytics page also displays recent invoices with:

* Invoice ID
* Shop
* Date
* Amount

The application displays up to the most recent 20 sales records.

---

# 💾 Data Storage

The current version does not use an external backend database.

It uses browser storage.

## Local Storage

The following data is stored:

```text
stockliveProducts
stockliveShops
stockliveSales
stockliveAccounts
```

Product information is loaded from `localStorage` when the application starts.

Shop information is also stored in Local Storage.

Sales information is loaded from Local Storage.

Account information is stored separately.

---

# 🔄 Data Persistence

When product, shop, or sales data changes, the application calls `saveData()`.

This saves:

```text
Products → Local Storage
Shops    → Local Storage
Sales    → Local Storage
```

Therefore, refreshing the browser does not automatically reset these stored values in the same browser profile.

---

# 🚦 Stock Status Logic

StockLive categorizes stock into three states.

## 🟢 Available

```text
Stock > 50
```

The system displays:

```text
AVAILABLE
```

## 🟡 Low Stock

```text
0 < Stock < 50
```

The system displays:

```text
LOW STOCK
```

## 🔴 Out of Stock

```text
Stock <= 0
```

The system displays:

```text
OUT OF STOCK
```

This logic is implemented through the `getStatus()` function.

---

# 🔄 Complete Application Workflow

The complete StockLive workflow is:

```text
                    START
                      │
                      ▼
                Login/Register
                      │
                      ▼
                  Dashboard
                      │
          ┌───────────┼───────────┐
          │           │           │
          ▼           ▼           ▼
      Inventory     Brands      Shops
          │           │           │
          └───────────┼───────────┘
                      │
                      ▼
               Retailer Billing
                      │
                      ▼
              Select Retailer
                      │
                      ▼
                Select Product
                      │
                      ▼
                 Enter Quantity
                      │
                      ▼
                Check Stock
                      │
              ┌───────┴────────┐
              │                │
           Available        Not Available
              │                │
              ▼                ▼
          Add to Bill       Show Error
              │
              ▼
           Complete Sale
              │
              ▼
        Deduct Stock Quantity
              │
              ▼
        Create Invoice Record
              │
              ▼
          Update Sales
              │
              ▼
        Sales Analytics
```

---

# 🛠️ Technology Stack

## HTML5

Used to create the application structure and different modules.

The page defines sections for login, dashboard, inventory, brands, billing, shops, and sales.

## CSS3

Used for:

* Layout
* Colors
* Cards
* Tables
* Buttons
* Responsive design
* Sidebar
* Login screen
* Status badges

The application defines CSS variables for primary colors, backgrounds, text, borders, success, warning, and danger states.

## JavaScript

JavaScript provides the application logic for:

* Login
* Registration
* Navigation
* Inventory
* Billing
* Shops
* Sales
* Storage
* Dashboard calculations

---

# 📂 Project Structure

The current project is implemented in a single HTML file:

```text
StockLive/
│
└── ssvtt.html
```

The file contains three major layers:

```text
ssvtt.html
│
├── HTML
│   ├── Login
│   ├── Registration
│   ├── Dashboard
│   ├── Inventory
│   ├── Brands
│   ├── Billing
│   ├── Shops
│   └── Sales Analytics
│
├── CSS
│   ├── Login Styles
│   ├── Dashboard Styles
│   ├── Table Styles
│   ├── Card Styles
│   ├── Billing Styles
│   └── Responsive Styles
│
└── JavaScript
    ├── Authentication
    ├── Product Data
    ├── Shop Data
    ├── Sales Data
    ├── Local Storage
    ├── Dashboard
    ├── Inventory
    ├── Billing
    ├── Shops
    └── Sales Analytics
```

---

# 📦 Product Catalog

The initial application contains seven products.

| No. | Product               | Brand     | Category   | Price | Initial Stock |
| --: | --------------------- | --------- | ---------- | ----: | ------------: |
|   1 | Colgate Salt 100g     | Colgate   | Toothpaste |   ₹79 |           713 |
|   2 | Colgate SF 9+3        | Colgate   | Toothbrush |  ₹240 |           800 |
|   3 | Godrej Fab            | Godrej    | Washing    |   ₹99 |           450 |
|   4 | Cinthol Health+       | Godrej    | Soap       |   ₹45 |           357 |
|   5 | Cinthol Lime          | Godrej    | Soap       |   ₹45 |           184 |
|   6 | Kellogg's Chocos      | Kellogg's | Cereal     |   ₹10 |           256 |
|   7 | Kellogg's Corn Flakes | Kellogg's | Cereal     |   ₹55 |            75 |

These values come from the initial product dataset in the project.

---

# 🏪 Initial Retailer Data

The application starts with two retailer shops:

| Retailer           | Location   | Contact    |
| ------------------ | ---------- | ---------- |
| Sri Murugan Stores | Madurai    | 9876543210 |
| SS Super Market    | Coimbatore | 9876543211 |

Additional shops can be added through the application.

---

# ▶️ How to Run the Project

## Method 1 — Open Directly

1. Save the project file as:

```text
ssvtt.html
```

2. Locate the file.
3. Double-click it.
4. The application opens in your default browser.

---

## Method 2 — Using VS Code

### Step 1

Install Visual Studio Code.

### Step 2

Create a project folder:

```text
StockLive
```

### Step 3

Place:

```text
ssvtt.html
```

inside the folder.

### Step 4

Open the folder in VS Code.

### Step 5

Open `ssvtt.html`.

### Step 6

Run it using a browser or the Live Server extension.

---

# 👤 How to Use the Application

## Step 1 — Create Account

Click:

```text
Create Account
```

Enter:

```text
Full Name
Gmail Address
Password
Confirm Password
```

Then click:

```text
Create Account
```

---

## Step 2 — Login

Enter your registered:

```text
Gmail
Password
```

Click:

```text
Login
```

---

## Step 3 — View Dashboard

After successful login, the Dashboard opens.

You can see:

```text
Total Products
Stock Units
Low Stock
Out of Stock
```

---

## Step 4 — Check Inventory

Open:

```text
Inventory
```

Search for a product if required.

---

## Step 5 — Manage Retailers

Open:

```text
Retailer Shops
```

Click:

```text
+ Add Shop
```

Enter the retailer information.

---

## Step 6 — Create Bill

Open:

```text
Retailer Billing
```

Select:

```text
Retailer
Product
Quantity
```

Click:

```text
+ Add Product
```

---

## Step 7 — Complete Sale

Review the bill.

Click:

```text
✓ Complete Sale
```

The system then:

```text
Deducts Stock
       ↓
Updates Retailer Orders
       ↓
Creates Invoice
       ↓
Stores Sale
       ↓
Updates Analytics
```

---

# 🛡️ Security Implementation

The project includes several frontend validation mechanisms.

### Gmail Validation

The registration process checks that the email follows a Gmail format.

### Password Validation

A minimum password length of six characters is required.

### Password Confirmation

The password and confirmation fields must match.

### Duplicate Account Prevention

The application checks whether the email already exists.

### Session Management

The login state is maintained using browser session storage.

### HTML Escaping

User-provided values displayed in generated HTML are passed through an `escapeHTML()` helper to escape characters such as `<`, `>`, `"`, and `'`.

---

# 📱 Responsive Design

StockLive contains responsive CSS rules.

For screens below 1000px:

* Dashboard cards change layout.
* Two-column sections become single-column.
* Brand cards become two-column.

For screens below 750px:

* Sidebar becomes collapsible.
* Main content uses the full screen.
* Mobile menu becomes visible.
* Dashboard cards become single-column.
* Brand and sales cards become single-column.

---

# 🎨 User Interface

The application uses a modern dashboard-style interface.

Major UI elements include:

```text
Login Card
Sidebar Navigation
Top Navigation Bar
Dashboard Cards
Data Tables
Brand Cards
Billing Panels
Sales Cards
Status Badges
Toast Notifications
```

The primary interface uses a blue-based color system with separate visual states for success, warning, and danger.

---

# 🔔 Notification System

StockLive uses toast notifications to provide feedback.

Examples include:

```text
Account created successfully.
Product added successfully.
Retailer shop added.
Product added to bill.
Sale completed successfully.
Dashboard refreshed.
Invalid login.
```

The toast component appears temporarily and automatically disappears after a short period.

---

# 🔄 Application Initialization

When the page loads, the application checks whether a valid session already exists.

If the user has a stored active session:

```text
Browser Opens
     ↓
Check Session
     ↓
Session Found
     ↓
Open Application
```

Otherwise:

```text
Browser Opens
     ↓
No Active Session
     ↓
Show Login
```

This behavior is implemented through the `DOMContentLoaded` event.

---

# 🧪 Testing Scenarios

The following scenarios can be tested during a project demonstration.

## Test 1 — Account Creation

**Input:** Valid name, Gmail, matching password.

**Expected Result:**

```text
Account created successfully.
```

---

## Test 2 — Invalid Gmail

**Input:** Non-Gmail email.

**Expected Result:**

```text
Please use a valid Gmail address.
```

---

## Test 3 — Password Mismatch

**Input:** Different password and confirmation.

**Expected Result:**

```text
Passwords do not match.
```

---

## Test 4 — Invalid Login

**Input:** Incorrect Gmail/password.

**Expected Result:**

```text
Invalid login.
```

---

## Test 5 — Add Product

Enter valid product details.

**Expected Result:**

Product appears in inventory.

---

## Test 6 — Add Retailer

Enter shop information.

**Expected Result:**

Retailer appears in the Shops module.

---

## Test 7 — Create Bill

Select retailer, product, and quantity.

**Expected Result:**

Product appears in the current bill.

---

## Test 8 — Excess Quantity

Request more units than available.

**Expected Result:**

The application rejects the quantity.

---

## Test 9 — Complete Sale

Complete a valid bill.

**Expected Result:**

```text
Stock decreases
+
Retailer order count increases
+
Invoice is created
+
Sales statistics update
```

---

# 💼 Business Benefits

StockLive can support distribution operations by providing a unified workflow.

### Improved Visibility

Users can quickly see available stock.

### Faster Billing

Retailer bills can be prepared digitally.

### Reduced Manual Calculation

Stock deduction is performed automatically after completed sales.

### Retailer Management

Retailer information can be maintained in one place.

### Sales Monitoring

Revenue and order statistics are automatically calculated.

### Low Stock Identification

Products requiring attention can be identified through stock-status indicators.

---

# ⚠️ Current Limitations

The current implementation is a **frontend prototype**.

It does not currently provide:

* Centralized server database
* Multi-user synchronization
* Server-side authentication
* Password hashing
* Cloud inventory synchronization
* Real-time communication between multiple devices
* Online payment integration
* PDF invoice generation
* Role-based permissions
* Server-side API

The current implementation stores data in the browser's Local Storage and login state in Session Storage.

Therefore, it should be considered a **prototype/demo application rather than a production distribution platform**.

---

# 🔮 Future Enhancements

The project can be expanded into a full-scale distribution management platform.

## 1. Backend Development

Possible technologies:

```text
Node.js
Express.js
Java Spring Boot
Python Django
Python Flask
```

---

## 2. Database Integration

Possible databases:

```text
MySQL
PostgreSQL
MongoDB
Firebase
```

A centralized database would allow multiple sales officers to access the same inventory.

---

## 3. Real-Time Inventory

A future version could provide:

```text
Sales Officer A
       │
       ▼
 Central Database
       ▲
       │
Sales Officer B
```

When one officer completes a sale, other authorized users could receive the updated stock information.

---

## 4. Role-Based Access

Possible roles:

```text
Admin
Distributor
Sales Officer
Warehouse Manager
Accountant
```

Different roles could receive different permissions.

---

## 5. Advanced Analytics

Future dashboards could include:

* Daily sales
* Weekly sales
* Monthly sales
* Brand-wise sales
* Product-wise sales
* Retailer-wise sales
* Top-selling products
* Low-stock trends

---

## 6. Notifications

Possible notifications:

```text
Low Stock Alert
Out of Stock Alert
New Retailer Order
Invoice Generated
Stock Updated
```

---

## 7. Mobile Application

A dedicated Android/iOS application could allow sales officers to use StockLive during field visits.

---

## 8. PDF Invoice

Future versions could generate downloadable invoices containing:

```text
Company Information
Retailer Information
Invoice Number
Date
Products
Quantity
Price
Total
```

---

## 9. GPS-Based Field Visits

A future field-sales module could record:

```text
Sales Officer
     ↓
Retailer Location
     ↓
Visit
     ↓
Order
     ↓
Billing
```

---

## 10. Inventory Forecasting

Machine-learning models could potentially analyze historical sales and estimate future stock requirements.

---

# 🏗️ Suggested Production Architecture

A future full-stack version could use:

```text
                 ┌────────────────────┐
                 │   Web / Mobile UI  │
                 └─────────┬──────────┘
                           │
                           ▼
                 ┌────────────────────┐
                 │     REST API       │
                 └─────────┬──────────┘
                           │
             ┌─────────────┼─────────────┐
             ▼             ▼             ▼
        Authentication  Inventory      Billing
             │             │             │
             └─────────────┼─────────────┘
                           ▼
                 ┌────────────────────┐
                 │      Database      │
                 └────────────────────┘
                           │
                           ▼
                 ┌────────────────────┐
                 │ Analytics / Reports│
                 └────────────────────┘
```

---

# 📊 Project Data Flow

```text
USER
 │
 ▼
LOGIN
 │
 ▼
DASHBOARD
 │
 ├──────────────► INVENTORY
 │                    │
 │                    ▼
 │                STOCK DATA
 │
 ├──────────────► SHOPS
 │                    │
 │                    ▼
 │                RETAILERS
 │
 └──────────────► BILLING
                      │
                      ▼
                SELECT PRODUCTS
                      │
                      ▼
                 CHECK STOCK
                      │
                      ▼
                 CREATE BILL
                      │
                      ▼
                 COMPLETE SALE
                      │
          ┌───────────┴───────────┐
          ▼                       ▼
    UPDATE STOCK            CREATE INVOICE
          │                       │
          └───────────┬───────────┘
                      ▼
                SALES ANALYTICS
```

---

# 🎓 Academic Project Information

## Project Title

**StockLive — Smart Distribution Inventory & Retailer Billing System**

## Organization

**SSVT Traders**

## Project Type

**Web-Based Distribution Management System**

## Domain

**Inventory Management / Distribution / Retail Billing**

## Frontend

**HTML5 + CSS3 + JavaScript**

## Storage

**Browser Local Storage / Session Storage**

---

# 📝 Project Description for College Report

StockLive is a web-based distribution management system developed to simplify inventory monitoring, retailer management, billing, and sales analysis.

The system allows users to register and log in using Gmail credentials. After authentication, the user can access a dashboard displaying product and stock statistics.

The inventory module provides information about products, brands, prices, stock quantities, and stock status. The system supports products from Colgate, Godrej, and Kellogg's.

The retailer billing module allows a sales officer to select a retailer, choose products, enter quantities, and create a bill. Before adding products, the system verifies their available stock. When a sale is completed, the sold quantity is automatically deducted from inventory and an invoice record is created.

The sales analytics module calculates total revenue, total orders, and average order value. Retailer shops can also be added and managed through the application.

The current implementation uses browser Local Storage for data persistence and Session Storage for login-session information, making it suitable as a frontend prototype and academic demonstration.

---

# 🎤 Short Project Explanation

> **StockLive is a smart distribution inventory and retailer billing system developed for SSVT Traders. The main purpose of the system is to help sales officers easily check product availability, manage retailer shops, create bills, and track sales. The system contains modules for login, dashboard, inventory, brands, retailer shops, billing, and sales analytics. During billing, the system checks stock availability and automatically reduces the stock after completing a sale. This helps reduce manual calculation and provides a structured digital workflow for distribution operations.**

---

# 📌 Key Project Highlights

```text
✅ Gmail-based Registration
✅ Login & Session Management
✅ Dashboard
✅ Inventory Management
✅ Product Search
✅ Stock Status Monitoring
✅ Colgate Products
✅ Godrej Products
✅ Kellogg's Products
✅ Retailer Management
✅ Retailer Billing
✅ Quantity Validation
✅ Automatic Stock Depletion
✅ Invoice Records
✅ Sales Analytics
✅ Revenue Calculation
✅ Responsive Design
✅ Local Storage
✅ Toast Notifications
```

---

# 📈 Expected Project Impact

The system is intended to provide a more organized digital workflow for distribution activities.

### Before

```text
Manual Stock Checking
        ↓
Manual Order Calculation
        ↓
Manual Billing
        ↓
Manual Stock Reduction
        ↓
Manual Sales Tracking
```

### With StockLive

```text
Digital Inventory
        ↓
Product Selection
        ↓
Automated Bill Calculation
        ↓
Automatic Stock Depletion
        ↓
Invoice Record
        ↓
Sales Analytics
```

---

# 🌟 Project Outcome

StockLive demonstrates how a web-based application can combine several distribution activities into one interface.

The current prototype successfully brings together:

**Inventory + Retailers + Billing + Stock Management + Sales Analytics**

into a single application.

The architecture can subsequently be extended with a backend, centralized database, multi-user synchronization, advanced analytics, notifications, and mobile support.

---

# 📜 License

This project is intended primarily for **educational, academic, demonstration, and prototype purposes**.

The project can be modified and extended according to academic or development requirements.

---

# 👨‍💻 Project Name

## StockLive — SSVT Traders

### Smart Distribution Inventory & Retailer Billing System

**Tagline:**

> **Know Your Stock. Bill Faster. Sell Smarter.**

---

## ⭐ Final Summary

StockLive is a digital distribution management prototype designed around the workflow of a sales officer.

The system starts with user authentication and provides access to a dashboard where inventory information can be monitored. Users can manage products, view brands, add retailer shops, prepare retailer bills, and complete sales.

The most important operational flow is:

```text
Retailer Visit
      ↓
Select Retailer
      ↓
Select Products
      ↓
Check Available Stock
      ↓
Enter Quantity
      ↓
Generate Bill
      ↓
Complete Sale
      ↓
Automatically Deduct Stock
      ↓
Generate Invoice Record
      ↓
Update Sales Analytics
```

This makes StockLive a suitable foundation for a larger **distribution, inventory, retailer billing, and field-sales management platform**.
