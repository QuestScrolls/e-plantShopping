# 🌿 Paradise Nursery — Plant Store (React + Redux)

A responsive single‑page web application for browsing and shopping a wide variety of indoor plants, built with **React** and **Redux Toolkit**. Users can explore plants by category, add them to a cart, adjust quantities, and view the total cost. The app also includes an **About Us** section and a smooth landing‑to‑product view transition.

![React](https://img.shields.io/badge/React-18-blue?logo=react)
![Redux Toolkit](https://img.shields.io/badge/Redux_Toolkit-^2-purple?logo=redux)
![Vite](https://img.shields.io/badge/Vite-5.2-646CFF?logo=vite)

---

## 📚 Project Origin
This project was developed as part of a **hands‑on lab** on Coursera:  
**"Building a Plant Store with React and Redux"** (or replace with the exact course name).  
The assignment provided a starter structure; I then completed missing parts, added styling, and enhanced functionality as described below.

---

## ✨ Features
- **Landing Page** with a welcoming message and a “Get Started” button that smoothly transitions to the product list.
- **Plant Catalogue** organised into 5 categories:
  - Air Purifying Plants
  - Aromatic Fragrant Plants
  - Insect Repellent Plants
  - Medicinal Plants
  - Low Maintenance Plants
- **Add to Cart**: instantly dispatches plant items to the Redux store.
- **Cart Management** (full Redux integration):
  - Increase / decrease item quantity.
  - Remove single items from cart.
  - Real‑time total amount calculation.
  - “Continue Shopping” and “Checkout” buttons.
- **About Us** page with mission statement (loaded directly on the landing page).
- **Responsive UI** with a custom navigation bar showing a cart icon and the total item count.

---

## 🛠️ Tech Stack
- **React 18** (functional components, hooks)
- **Redux Toolkit** (state management for cart)
- **React‑Redux** (Provider, useSelector, useDispatch)
- **Vite** (fast dev server and build tool)
- **Pure CSS** (component‑scoped styles)

---

## 📁 Project Structure

paradise-nursery/
├── public/
├── src/
│ ├── App.jsx # Main component, controls landing / product view
│ ├── App.css
│ ├── AboutUs.jsx # About Us content
│ ├── AboutUs.css
│ ├── ProductList.jsx # Plant catalogue & add‑to‑cart logic
│ ├── ProductList.css
│ ├── CartItem.jsx # Cart display, quantity controls, totals
│ ├── CartItem.css
│ ├── CartSlice.js # Redux slice (add, remove, updateQuantity)
│ ├── store.js # Redux store configuration
│ ├── main.jsx # ReactDOM entry, wraps App with Provider
│ └── index.css
├── index.html
├── package.json
├── vite.config.js
└── README.md


---

## 🚀 Getting Started

### Prerequisites
- Node.js (v18 or higher)
- npm (v9+)

### Installation
            ```bash
            git clone https://github.com/QuestScrolls/paradise-nursery.git
            cd paradise-nursery
            npm install
            npm run dev
            npm run build
            npm run preview   # to preview the production build locally
            
🧠 How It Works
State Management (Redux)

  CartSlice defines the items array and three reducers:

  addItem – If the item already exists, increase quantity; otherwise add it with quantity = 1.

  removeItem – Removes the item by name.

  pdateQuantity – Directly sets the quantity for a given item.

  The store is created in store.js and passed to the app via <Provider> in main.jsx.

Key Components

  App.jsx – Manages whether to show the landing page or product list using local state showProductList. Clicking “Get Started” toggles to products.

  ProductList.jsx – Displays all plants grouped by category. Contains the handleAddToCart function that dispatches addItem and updates local “added” state.

  CartItem.jsx – Reads cart items from the Redux store, calculates totals, and dispatches updateQuantity / removeItem. The cart icon on the navbar shows the total item count.

  AboutUs.jsx – Purely presentational component with the nursery’s mission text.

📝 Modifications & Improvements (from original lab)

  Completed the Cart slice implementation.

  Added category headings and structured plant data.

  Implemented total quantity badge on cart icon.

  Enhanced landing page with responsive layout.

  Added About Us section directly on the landing page.

  Planned: Add a proper checkout flow (e.g., form validation).

  Planned: Implement React Router for separate pages.

  Planned: Connect to a backend API for plant data.

🙏 Credits

  Original lab & starter code: Coursera course “Build a Plant Store with React and Redux” (or actual course name)

  Modifications & documentation: [Your Name]

⚖️ Academic Integrity Note

This repository is a finished version of a course assignment, shared for portfolio and learning purposes. If you are currently enrolled in the same lab, please use this code only as a reference after completing your own work, in line with your course’s academic integrity policy.


