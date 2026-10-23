# 🌿 Organic Solution: Frontend

React frontend for **Organic Solution**, an E-Commerce platform for organic products (dates, nuts, honey, dried fruits and more). It provides a complete shopping experience: browsing, search, cart, checkout and an admin panel, powered by a Django REST API.

🔗 **Live Demo:** https://organic-solution-pqrs.vercel.app/

⚙️ **Backend Repo:** https://github.com/rezasdsju/emarket/tree/main/backend

---

## ✨ Features

- **Home page** with featured products
- **Product catalog**: all products, category-wise listing and product detail pages
- **Smart search** with a search bar and a dedicated search results page
- **Shopping cart** with global state management (Context API)
- **Checkout & payment** flow connected to the order and payment APIs
- **Admin login and admin panel** for managing the store
- **Responsive design** built with Bootstrap, works on mobile, tablet and desktop
- **Clean, feature-based architecture** that is easy to scale and maintain

---

## 🛠️ Tech Stack

| Category | Technology |
|---|---|
| Library | React 19 |
| Routing | React Router v7 |
| HTTP Client | Axios |
| UI | Bootstrap 5, React-Bootstrap |
| State Management | React Context API |
| Build Tool | Create React App (`react-scripts`) |
| Testing | React Testing Library, Jest |
| Deployment | Vercel |

---

## 📁 Project Structure

```
organic-solution-frontend/
├── public/
│   ├── favicon.ico
│   ├── index.html
│   ├── manifest.json
│   └── robots.txt
├── src/
│   ├── app/                  # App entry and route configuration
│   │   ├── App.js
│   │   └── routes.js
│   ├── assets/               # Images and icons
│   ├── components/
│   │   ├── layout/           # Navbar, Footer
│   │   └── ui/               # Reusable UI (Button, LoadingSpinner)
│   ├── features/             # Feature-based modules
│   │   ├── admin/            # AdminLogin, AdminPanel
│   │   ├── cart/             # Cart
│   │   ├── catalog/          # Products, categories, search, product detail
│   │   ├── checkout/         # Payment
│   │   ├── home/             # Home
│   │   └── about/            # About
│   ├── context/              # CartContext
│   ├── hooks/                # Custom hooks
│   ├── services/             # API layer (api, productService, categoryService)
│   ├── utils/                # Helper functions
│   ├── styles/               # Global styles
│   └── index.js
├── .env.example
├── package.json
└── README.md
```

The project follows a **feature-based structure**: each feature (catalog, cart, checkout, admin) keeps its own components together, while shared pieces live in `components/`, and all API calls are isolated in `services/`.

---

## 🚀 Getting Started

### Prerequisites

- Node.js 18 or higher
- npm
- The [backend API](https://github.com/rezasdsju/emarket/tree/main/backend) running locally or deployed

### 1. Clone the repository

```bash
git clone https://github.com/rezasdsju/organic-solution-frontend.git
cd organic-solution-frontend
```

### 2. Install dependencies

```bash
npm install
```

### 3. Configure environment variables

Copy the example file and fill in your values:

```bash
cp .env.example .env
```

Set the backend API URL inside `.env` (use the variable name listed in `.env.example`):

```env
REACT_APP_API_URL=http://127.0.0.1:8000/api
```

> Variables used in Create React App must start with `REACT_APP_`. Restart the dev server after changing `.env`.

### 4. Start the development server

```bash
npm start
```

The app runs at `http://localhost:3000`.

---

## 📜 Available Scripts

| Command | Description |
|---|---|
| `npm start` | Run the app in development mode |
| `npm run build` | Create an optimized production build in `build/` |
| `npm test` | Run tests in watch mode |

---

## 🔌 Backend Integration

The frontend communicates with the Django REST API through Axios (see `src/services/`). Main endpoints used:

| Purpose | Endpoint |
|---|---|
| Categories | `GET /api/categories/` |
| Products | `GET /api/products/` |
| Featured products | `GET /api/products/featured/` |
| Products by category | `GET /api/products/by_category/?category_slug=<slug>` |
| Search | `GET /api/search/?q=<term>` |
| Autocomplete | `GET /api/search/autocomplete/?q=<term>` |
| Place order | `POST /api/orders/` |
| Payments | `POST /api/payments/` |

Make sure the backend has CORS enabled for your frontend domain.

---

## ☁️ Deployment (Vercel)

1. Push the project to GitHub.
2. Import the repository in [Vercel](https://vercel.com).
3. Add the environment variable `REACT_APP_API_URL` pointing to your deployed backend.
4. Deploy. Vercel detects Create React App automatically.

For client-side routing to work on refresh, add a `vercel.json` in the project root:

```json
{
  "rewrites": [{ "source": "/(.*)", "destination": "/index.html" }]
}
```

---

## 🗺️ Roadmap

- [ ] Token-based admin authentication (JWT)
- [ ] User accounts and order history
- [ ] Wishlist and product reviews
- [ ] Image lazy loading and performance optimization
- [ ] SEO improvements (Open Graph tags, meta descriptions)
- [ ] Unit and integration tests
- [ ] Migration from Create React App to Vite

---

## 🤝 Contributing

Suggestions and pull requests are welcome. Please open an issue first to discuss major changes.

## 📄 License

This project is built for learning and portfolio purposes. Add a license of your choice (e.g. MIT) before distributing.

---

## 👤 Author

**Rezaul Karim Rifat**
GitHub: [@rezasdsju](https://github.com/rezasdsju)
Live Demo: https://organic-solution-pqrs.vercel.app/