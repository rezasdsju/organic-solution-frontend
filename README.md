# 🌿 Organic Solution: Frontend

React frontend for **Organic Solution**, an e-commerce store for organic products (dates, nuts, honey, dried fruits and more). It lets customers browse and search products, add them to a cart and place orders, while an admin panel handles store management. The app consumes a Django REST Framework API.

🔗 **Live Demo:** https://organic-solution-pqrs.vercel.app/

⚙️ **Backend Repo:** https://github.com/rezasdsju/emarket/

---

## ✨ Features

- **Home page** to start browsing the store
- **All products** page and **category-wise** product listing
- **Product detail** page for each item
- **Search** with a search bar and a dedicated search results page
- **Shopping cart**
- **Payment page** to complete the order
- **Admin login and admin panel** for store management
- **About page**

---

## 🛠️ Tech Stack

| Category | Technology |
|---|---|
| Library | React 19 |
| Routing | React Router DOM 7 |
| HTTP Client | Axios |
| UI | Bootstrap 5, React-Bootstrap |
| Build Tool | Create React App (`react-scripts` 5) |
| Testing | React Testing Library, Jest |
| Deployment | Vercel |

---

## 📁 Project Structure

```
organic-solution-frontend/
├── .gitignore
├── README.md
├── package.json
├── package-lock.json
├── public/
│   ├── favicon-1.ico
│   ├── favicon.ico
│   ├── index.html
│   ├── logo192.png
│   ├── logo512.png
│   ├── manifest.json
│   └── robots.txt
└── src/
    ├── App.css
    ├── App.js
    ├── App.test.js
    ├── index.css
    ├── index.js
    ├── logo.svg
    ├── reportWebVitals.js
    ├── setupTests.js
    └── components/
        ├── About.js
        ├── AdminLogin.js
        ├── AdminPanel.js
        ├── AllProducts.js
        ├── Cart.js
        ├── CategoryProducts.js
        ├── Home.js
        ├── Navbar.js
        ├── Payment.js
        ├── ProductCard.js
        ├── ProductDetail.js
        ├── SearchBar.js
        └── SearchResults.js
```

---

## 🚀 Getting Started

### Prerequisites

- Node.js 20 or higher (required by React Router 7)
- npm
- The [backend API](https://github.com/rezasdsju/emarket/tree/main/backend) running locally or deployed

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/rezasdsju/organic-solution-frontend.git
cd organic-solution-frontend

# 2. Install dependencies
npm install

# 3. Start the development server
npm start
```

The app runs at `http://localhost:3000`.

### Connecting to the backend

Run the Django backend (by default at `http://127.0.0.1:8000`) and make sure the API base URL used in the frontend's Axios requests points to it. The backend must also allow requests from your frontend origin (CORS).

---

## 📜 Available Scripts

| Command | Description |
|---|---|
| `npm start` | Run the app in development mode |
| `npm run build` | Create a production build in `build/` |
| `npm test` | Run tests in watch mode |
| `npm run eject` | Eject from Create React App (one-way) |

---

## ☁️ Deployment

The frontend is deployed on **Vercel**. To deploy your own copy, import the repository in Vercel and point the app to your deployed backend API.

---

## 👤 Author

**Rezaul Karim Rifat**
GitHub: [@rezasdsju](https://github.com/rezasdsju)
Portfolio: [rezaul-karim-rifat-portfolio.vercel.app](https://rezaul-karim-rifat-portfolio.vercel.app/)