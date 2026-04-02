# FinTrack — Finance Dashboard UI

> **Live Demo:** https://Harshitha-Medipelly.github.io/finance-dashboard/

A modern, responsive, and feature-rich finance dashboard built using **React 18, Vite, Tailwind CSS, and Recharts**.
This project was developed as part of a frontend engineering evaluation and focuses on delivering clean UI, interactive data visualization, and a smooth user experience.

---

## 📸 Preview

| Dashboard                               | Transactions                                | Insights                       |
| --------------------------------------- | ------------------------------------------- | ------------------------------ |
| Financial overview with KPIs and charts | Filterable and sortable transaction records | Data-driven financial insights |

---

## ✨ Key Highlights

### 📊 Dashboard Overview

* Displays **four key metrics**: Total Balance, Income, Expenses, and Savings Rate
* Interactive **line chart** showing financial trends across 6 months
* **Donut chart** visualizing expense distribution by category
* Quick view of **recent transactions** with category-based styling

---

### 💳 Transaction Management

* Fully functional **paginated table** (10 entries per page)
* Advanced filtering:

  * Keyword search
  * Transaction type (Income / Expense)
  * Category selection
  * Custom date range
* **Sortable columns** (Date, Category, Amount)
* Dynamic **filter chips** with instant removal
* **Admin-only controls** for adding, editing, and deleting records

---

### 🔐 Role-Based Interface (Simulated)

| Capability       | Admin | Viewer |
| ---------------- | ----- | ------ |
| View data        | ✅     | ✅      |
| Add transactions | ✅     | ❌      |
| Modify entries   | ✅     | ❌      |
| Delete entries   | ✅     | ❌      |

Users can toggle roles instantly via the header. The selected role is stored locally for persistence.

---

### 📈 Insights & Analytics

* Identifies **top spending category** with percentage contribution
* Calculates **savings rate** and compares with recommended benchmarks
* Monthly **income vs expense comparison (bar chart)**
* Detailed **category-wise breakdown table** with progress indicators
* Automatically generated insights highlighting trends and patterns

---

### 🎨 User Experience & Design

* Built-in **dark mode** with persistent preference
* Data stored in **localStorage** for seamless offline usage
* Fully **responsive layout** with adaptive sidebar
* Meaningful **empty states** when no data is available
* Accessible modals with keyboard support (Esc to close)
* Smooth UI animations for better interaction

---

## 🛠️ Tech Stack

| Technology               | Purpose                           |
| ------------------------ | --------------------------------- |
| React 18                 | Component-based UI development    |
| Vite 5                   | Fast build tool and dev server    |
| Tailwind CSS 3           | Utility-first styling and theming |
| Recharts 2               | Data visualization (charts)       |
| React Router 6           | Page navigation                   |
| Lucide React             | Icon system                       |
| Context API + useReducer | Global state management           |
| localStorage             | Client-side persistence           |

---

## ⚙️ Local Setup

```bash
# Clone your repository
git clone https://github.com/Harshitha-Medipelly/finance-dashboard.git

# Navigate to project
cd finance-dashboard

# Install dependencies
npm install

# Run development server
npm run dev
```

Visit: **http://localhost:5173**

---

## 📂 Project Architecture

```
src/
├── main.jsx
├── App.jsx
├── index.css

├── data/
│   └── mockData.js

├── utils/
│   └── finance.js

├── context/
│   └── AppContext.jsx

├── components/
│   ├── Layout/
│   ├── Dashboard/
│   ├── Transactions/
│   └── Insights/

└── pages/
```

---

## 🔄 State Management Approach

The application uses **React Context with useReducer**, enabling scalable and maintainable global state without external libraries.

### Core State:

* `transactions` → stored in localStorage
* `role` → admin or viewer
* `darkMode` → theme preference
* `filters` → search and sorting controls
* `modal` → form state

### Derived State:

* Filtered transactions computed efficiently using `useMemo`

---

## 📊 Mock Dataset

* Contains **75+ transactions** spanning 6 months
* Covers multiple income and expense categories
* Automatically initialized and persisted in localStorage

---

## 🚀 Deployment

The project is deployed using **GitHub Pages with CI/CD automation**.

### Workflow:

* Install dependencies
* Build production bundle
* Deploy `dist/` automatically on push

🔗 Live App:
https://Harshitha-Medipelly.github.io/finance-dashboard/

---

## 🎯 Project Objective

Managing finances can be complex without proper visualization tools.
This dashboard simplifies financial tracking by providing clear insights, structured data, and interactive analytics.

---

## 🔮 Future Enhancements

* Backend integration (Node.js + MongoDB)
* Authentication system (JWT-based login)
* AI-powered financial insights and predictions
* Export data (CSV / PDF reports)
* Real-time data synchronization

---

## 📌 Assumptions

* Currency used: USD
* Role system is frontend-simulated
* Works fully offline with mock data
* Insights calculated assuming current date: April 2026

---
