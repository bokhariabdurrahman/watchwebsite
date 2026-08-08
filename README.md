# KICKZONE - Premium Sneaker Selling Web Application

An ultra-premium, interactive, and responsive web application designed for a Sneaker Selling Store. This project features a dark-themed, glassmorphic design system with custom micro-animations and robust client-side interactions.

---

## 🌟 Pages & Key Features

1. **Landing Page (`index.html`)**
   - Premium sticky glassmorphic navigation bar.
   - Dynamic cart quantity badge that updates in real-time across tabs.
   - Interactive hero section with floating sneaker graphic and rotational light animation.
   - Revolutionary tech-highlights section.
   - Live Featured Products grid displaying best-selling models.
   
2. **Product Catalog Page (`products.html`)**
   - Live Search: Filter sneakers in real-time by keyword.
   - Comprehensive Filter Sidebar:
     - Filter by brands (Nike, Adidas, Jordan, Yeezy).
     - Live interactive Price Range slider (up to $300).
     - Interactive size selection grid.
   - Dynamic sorting: Sort by price (low to high, high to low) and rating.
   - **Quick View Modal**: Clicking a sneaker opens a modal displaying detailed product information, active colorways selector, size selection chips, quantity adjustment controls, and an "Add to Cart" button.
   - Deep Linking support: Appending `?id=X` (e.g., `products.html?id=3`) directly launches the Quick View modal for that specific sneaker.

3. **Shopping Cart View Page (`cart.html`)**
   - Lists all selected sneakers, brand, price, selected size, and colorway.
   - Size/Quantity control buttons allowing users to increase, decrease, or remove items.
   - Live checkout calculations updating subtotals, tax (8%), shipping costs (free above $200, else $15), and grand totals.
   - Promo Code Section: Entering the promo code **`SNEAKER15`** applies a live 15% discount.
   - Dynamic empty cart fallback.

4. **Payment Page (`payment.html`)**
   - Secure checkout layout with shipping details and payment forms.
   - Interactive payment methods selector (Credit Card vs. PayPal).
   - Real-time client-side form validation ensuring correct name, email format, shipping address, zip codes, cardholder name, card number formatting, CVV, and expiry fields.
   - Custom credit card input formatting (automatically formats numbers into four-digit chunks `xxxx xxxx xxxx xxxx` and inserts `/` for expiries).
   - Beautiful **Order Confirmed Success Modal** rendering transaction IDs, total paid amount, recipient info, and clearing the cart on checkout completion.

---

## 🚀 How to Run Locally

You can run this application by starting a local HTTP server inside the project root:

```bash
# Using Python
python -m http.server 8000
```

Now, navigate to `http://localhost:8000` in your web browser.

Alternatively, you can open any of the HTML pages directly by double-clicking them in your file explorer.

---

## 📁 Project Directory Structure

```
sneakersellingwebsite/
├── assets/
│   ├── sneaker_airmax.png       # DALL-E generated premium sneaker image
│   ├── sneaker_ultraboost.png   # DALL-E generated premium sneaker image
│   ├── sneaker_jordan.png       # DALL-E generated premium sneaker image
│   └── sneaker_yeezy.png        # DALL-E generated premium sneaker image
├── css/
│   └── style.css                # Central stylesheets, glassmorphic styles & animations
├── js/
│   ├── data.js                  # Sneaker inventory mock database
│   └── cart-manager.js          # Cart storage, state management, and utility functions
├── index.html                   # Landing page
├── products.html                # Catalog page
├── cart.html                    # Cart page
├── payment.html                 # Payment and Checkout page
└── README.md                    # Project documentation
```

---

## 📤 How to Upload to GitHub

We have initialized a local Git repository. To push the code to your GitHub account:

1. Create a new repository on your GitHub account (do **not** initialize it with a README or `.gitignore` since they are already included here).
2. Open your terminal in the project directory and run:

```bash
# Add files to staging
git add .

# Commit changes
git commit -m "Initial commit: Sneaker store web application"

# Rename branch to main
git branch -M main

# Link your remote repository (replace with your GitHub URL)
git remote add origin https://github.com/<YOUR-USERNAME>/<YOUR-REPO-NAME>.git

# Push to GitHub
git push -u origin main
```
