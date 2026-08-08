# CHRONOZONE - Premium Watch Selling Web Application

An ultra-premium, interactive, and responsive full-stack web application designed for a luxury watch boutique. This project showcases a sleek, dark-themed, glassmorphic design system with customized micro-animations, a robust Express backend API, and a live MongoDB Atlas cloud database connection.

---

## 🌟 Pages & Key Features

1. **Landing Page (`index.html`)**
   - Premium sticky glassmorphic navigation bar.
   - Dynamic cart quantity badge that updates in real-time.
   - Interactive hero section with rotational light animation featuring premium watch graphics.
   - History section highlighting the shop's heritage: **"Established in 2007 (Exiting since 19 Years)"**.

2. **Product Catalog Page (`products.html`)**
   - Live Search: Filter timepieces in real-time by keyword.
   - Brand Filters: Filter by collection series (**G-Shock**, **Casio Vintage**, **Casio Youth**).
   - Price Filter: Live interactive Price Range slider (up to ₹30,000 INR).
   - **Direct-to-Payment Buy Flow**: Clicking the **"Buy"** button instantly adds the watch to the shopping cart and routes the buyer straight to the payment checkout page.
   - **View Detail Modal**: If a product is sold out, clicking "View" opens a detailed specification sheet with dial colorway pickers.

3. **Shopping Cart View Page (`cart.html`)**
   - Lists selected watches, pricing, quantity, and dial colors.
   - Live checkout calculations updating subtotals, tax (8%), shipping costs (free above ₹15,000, else ₹300), and grand totals.
   - Coupon Engine: Validate custom promotional codes (e.g. **`WATCH15`**) directly against database storage.

4. **Payment Page (`payment.html`)**
   - Secure checkout layout with shipping details, OTP authentication verification, and payment methods.
   - Pre-payment confirmation modal to authorize card/UPI transactions.
   - Full-width, official, printable **Payment Success Invoice Bill** showing customer billing details, order items list, total calculation breakdown, and transaction status.

5. **Administrator Dashboard (`admin.html`)**
   - Secured via admin validation checks (admin phone: `93467 57938`, OTP code: `9534`).
   - Sales Bills list showing all historical invoices recorded on the database.
   - Stock Controller to toggle watch stock status (In Stock / Sold Out) in real-time.
   - Catalog Manager: Add new watches, edit details, set retail prices, set graphic themes, and customize dials.
   - Coupon Creator: Generate, list, and disable discount coupons directly on the database.

---

## 🛠️ Tech Stack & Architecture
* **Frontend**: HTML5, CSS3 (Vanilla), Vanilla JavaScript.
* **Backend**: Node.js & Express API Server.
* **Database**: MongoDB Atlas (Cloud Cluster).
* **Architecture**: Monolithic Web App (Express serves both the API routes and client assets).

---

## 🚀 How to Run Locally

1. Install dependencies inside the `server/` directory:
   ```bash
   cd server
   npm install
   ```
2. Configure environment variables in `server/.env`:
   ```env
   PORT=5000
   MONGODB_URI=mongodb+srv://abdurrahman:Syed%409534@watch.wa8wqrd.mongodb.net/watch?retryWrites=true&w=majority
   JWT_SECRET=chrono_secret_key_9534
   ```
3. Start the monolithic application:
   ```bash
   node server.js
   ```
4. Open your browser and navigate to:
   **`http://localhost:5000`**

---

## 📁 Project Directory Structure

```
sneakersellingwebsite/
├── assets/                       # High-res watch graphics
├── css/
│   └── style.css                 # Glassmorphic dark style sheets
├── js/
│   ├── config.js                 # API base URL settings
│   ├── data.js                   # Client data loader
│   └── cart-manager.js           # Client cart state controller
├── server/
│   ├── config/                   # Database setup
│   ├── models/                   # Mongoose schemas (Product, Order, User, Coupon)
│   ├── routes/                   # API routers (auth, products, admin, orders, cart)
│   ├── scripts/                  # DB seed controllers
│   ├── .env                      # Environment config variables
│   ├── package.json              # Server dependencies list
│   └── server.js                 # Monolithic entry point
├── index.html                    # Store landing page
├── products.html                 # Watch catalog
├── cart.html                     # Cart page
├── payment.html                  # Checkout page
├── login.html                    # OTP verification
├── admin.html                    # Admin dashboard portal
└── README.md                     # Documentation
```
