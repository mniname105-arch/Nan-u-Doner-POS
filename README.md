# Nan u Döner — POS System 🥙

A lightweight, fully offline-capable Point of Sale (POS) system built specifically for Nan u Döner. This application runs entirely in the browser using pure HTML, CSS, and JavaScript. No backend server or database setup is required—all data is securely stored directly on the device using `localStorage`.

## ✨ Features

* **Quick Menu & Cart:** Fast, touch-friendly interface designed for iPad and tablet use.
* **Order Checkout:** Calculates totals and change automatically.
* **Receipt Generation:** Automatically generates beautifully formatted receipts with your store logo, ready for thermal printing.
* **Daily Sales Tracking:** Keeps a running history of all orders for the day with the ability to clear or export them.
* **Expense Management:** Track daily operational costs (Meat, Bread, Gas, Staff, etc.) with custom descriptions and amounts.
* **Calendar & Reports:** A visual monthly calendar showing green (profit) and red (loss) days. Tap any day to see total sales, total expenses, net profit, and best-selling items.
* **Admin Panel:** Add, edit, or delete menu items and categories directly from the app. Upload item photos and your store logo.
* **Data Export:** Export your sales history to a CSV file for bookkeeping in Excel or Google Sheets.

## 📁 File Structure

To run this application, you only need two files in the same folder:
1. `index.html` - The main application code containing all HTML, CSS, and JavaScript.
2. `image.png` - Your custom store logo (the app will look for this exact filename to display in the header and on printed receipts).

## 🚀 How to Run & Install

Because this app does not require a backend server, you have a few easy ways to run it:

### Option 1: Desktop / Laptop (Chrome or Edge)
1. Double-click `index.html` to open it in your browser.
2. **To install as an app:** Click the browser menu (three dots) -> **Save and share** -> **Install page as app** (or **Create Shortcut**). This will create a dedicated desktop shortcut.

### Option 2: iPad (100% Offline using Documents by Readdle)
1. Download the free **Documents by Readdle** app from the App Store.
2. Transfer the folder containing `index.html` and `image.png` to the Documents app.
3. Tap `index.html` inside the app to open the POS in full screen.

### Option 3: iPad (Add to Home Screen via GitHub Pages)
If you want the app right on your iPad home screen:
1. Create a free account on [GitHub](https://github.com/) and create a new repository.
2. Upload `index.html` and `image.png` to the repository.
3. Go to **Settings > Pages** and enable GitHub Pages from the `main` branch.
4. Open the generated live link in Safari on your iPad.
5. Tap the **Share** button and select **Add to Home Screen**. 

## ⚙️ Configuration & Data Reset

* **Adding Menu Items:** Go to the **Admin** tab to populate your menu.
* **Setting the Logo:** Go to **Admin > Settings** to upload or change the store logo. 
* **Data Storage:** Since data is stored in the browser's `localStorage`, clearing your browser's cache/history *will* delete your sales and menu data. Always use the **Export** feature to back up your sales data regularly!

## 🛠 Tech Stack
* **HTML5** (Structure)
* **CSS3** (Styling, custom CSS variables, responsive Grid/Flexbox)
* **Vanilla JavaScript** (Logic, DOM manipulation, DOM printing)
* **localStorage API** (Data persistence)
