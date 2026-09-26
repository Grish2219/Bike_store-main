# Bike Spare Parts E-Commerce Website

A complete, production-ready, professional Core PHP & MySQL E-Commerce web application for motorcycle spare parts, accessories, and lubricants.

- **Project Type:** MCA Mini Project
- **Author:** Grish A
- **Technology Stack:** PHP 8 (Core PHP with `mysqli`), MySQL, Bootstrap 5.3, JavaScript, Font Awesome 6, Google Fonts (Poppins), Chart.js, SweetAlert2
- **Environment:** XAMPP Compatible (Apache & MySQL)

---

## 🌟 Key Features

### 🛒 Customer Storefront
- **Responsive Modern UI:** Built with Bootstrap 5.3, custom CSS variables, and automotive red accent styling.
- **Hero Slider & Highlights:** Showcases top high-performance motorcycle components and store perks.
- **Dynamic Category & Brand Showcase:** Filter spare parts by categories (Braking Systems, Engine Parts, Chains & Sprockets, Tires & Wheels, Oils & Lubricants) and brands (Brembo, Yamaha, Honda, Akrapovič, Motul, Dunlop).
- **Product Catalog with Filters & Pagination:** Interactive sidebar for real-time category/brand filtering, search keyword matching, price/name sorting, and page pagination.
- **Product Detail Page:** Multi-thumbnail gallery viewer, stock status indicator badges, quantity counter control, full specifications, and related spare part recommendations.
- **Session & Database Cart:** Seamless cart persistence across sessions, item quantity updates (`+` / `-`), auto subtotal calculations, free shipping threshold counter (orders >= ₹2,999), and SweetAlert item removal confirmations.
- **Checkout & Invoice Generator:** Multi-step shipping address form, payment method selector (COD & UPI Mock), order total verification, stock deduction, and printable order confirmation invoice.
- **Customer Lifecycle:** User registration, password hashing (`password_hash`), authentication, profile management, and complete order history tracking.

### 🛡️ Administrative Panel (Dark Theme)
- **Dark Aesthetic Dashboard:** Metric summary cards (Total Products, Categories, Brands, Customers, Total Orders, Revenue) and monthly sales analytics bar chart powered by Chart.js.
- **Product Inventory Module:** Full CRUD operations for spare parts with image uploads, category/brand selectors, stock tracking, and status toggles.
- **Category Module:** Create, read, update, and delete categories with image uploads.
- **Brand Module:** Full CRUD management for brand partners with logo upload previews.
- **Customer Management:** View customer directory, account details, and purchase history.
- **Order Management:** Filter orders by state (`Pending`, `Processing`, `Delivered`, `Cancelled`) and update order fulfillment / payment statuses.
- **Analytics & Reports:** Sales reports, top-selling spare parts rankings, category revenue distribution charts, and printable business summaries.

---

## 🔒 Security Implementation

- **Database Safety:** Prepared Statements using `mysqli` (`prepare()`, `bind_param()`, `execute()`) preventing SQL Injection.
- **XSS Protection:** Input HTML escaping helper `e()`.
- **CSRF Defense:** Custom anti-CSRF token generation and session token verification across forms and GET action URLs.
- **Authentication Security:** Passwords encrypted using `password_hash()` with `PASSWORD_BCRYPT`.
- **Session Guards:** Strict page access guards (`require_customer()`, `require_admin()`).

---

## 🔑 Default Login Credentials

### Administrator Portal (`/admin/login.php`)
- **Username:** `admin` (or `admin@bikestore.com`)
- **Password:** `admin123`

### Demo Customer (`/login.php`)
- **Email:** `rahul@example.com`
- **Password:** `user123`

---

## 🚀 Setup & Installation Instructions (XAMPP)

1. **Download / Copy Project Folder**
   - Place the `Bike_store` folder into your XAMPP `htdocs` directory:
     ```text
     C:\xampp\htdocs\Bike_store
     ```

2. **Start XAMPP Modules**
   - Open **XAMPP Control Panel**.
   - Click **Start** for **Apache** and **MySQL**.

3. **Import Database (`bike_store.sql`)**
   - Open your web browser and navigate to: [http://localhost/phpmyadmin](http://localhost/phpmyadmin)
   - Click **Databases** tab and create a new database named `bike_store`.
   - Select `bike_store`, go to the **Import** tab.
   - Choose the file `bike_store.sql` located in the `Bike_store` root folder and click **Import**.

4. **Run the Application**
   - **Storefront:** [http://localhost/Bike_store/](http://localhost/Bike_store/)
   - **Admin Panel:** [http://localhost/Bike_store/admin/login.php](http://localhost/Bike_store/admin/login.php)

---

## 📁 Complete Folder Structure

```text
Bike_store/
├── admin/
│   ├── login.php
│   ├── logout.php
│   ├── dashboard.php
│   ├── header.php
│   ├── footer.php
│   ├── sidebar.php
│   ├── products.php
│   ├── add_product.php
│   ├── edit_product.php
│   ├── delete_product.php
│   ├── categories.php
│   ├── add_category.php
│   ├── edit_category.php
│   ├── delete_category.php
│   ├── brands.php
│   ├── add_brand.php
│   ├── edit_brand.php
│   ├── delete_brand.php
│   ├── customers.php
│   ├── customer_details.php
│   ├── orders.php
│   ├── order_details.php
│   └── reports.php
├── includes/
│   ├── db.php
│   ├── functions.php
│   ├── header.php
│   ├── navbar.php
│   └── footer.php
├── uploads/
│   └── (pre-populated placeholder images for all sample products, categories, and brands)
├── assets/
│   ├── css/
│   │   ├── style.css
│   │   └── admin.css
│   ├── js/
│   │   ├── main.js
│   │   └── admin.js
│   └── images/
│       └── logo.svg
├── index.php
├── shop.php
├── product.php
├── search.php
├── cart.php
├── add_to_cart.php
├── update_cart.php
├── remove_from_cart.php
├── checkout.php
├── register.php
├── login.php
├── logout.php
├── forgot_password.php
├── profile.php
├── my_orders.php
├── order_success.php
├── about.php
├── contact.php
├── 404.php
├── bike_store.sql
└── README.md
```

---

## 🎓 Project Credits
- **Developer:** Grish A
- **Course:** MCA Mini Project
- **License:** Open Source Educational Project
