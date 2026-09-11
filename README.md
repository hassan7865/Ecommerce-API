# Ecommerce-API

Node.js / Express REST API for a simple ecommerce store. Deployed on Vercel: [backend-ecommerce-plum.vercel.app](https://backend-ecommerce-plum.vercel.app).

Pairs with the storefront: [Ecommerce-Storefront](https://github.com/hassan7865/Ecommerce-Storefront).

## Overview

MongoDB-backed API for auth, users, products, carts, orders, and income stats. JWT protects authenticated routes; admin checks gate product/order management.

## Stack

- Node.js, Express
- MongoDB via Mongoose
- JSON Web Tokens + CryptoJS (password encryption)
- CORS, dotenv
- Optional Stripe dependency (present in `package.json`; wire via env if you use it)

## Structure

```
index.js           # App entry, CORS, route mounts
models/            # User, Product, Cart, Order
routes/            # auth, user, product, cart, order, income, VerifyToken
vercel.json        # Vercel deployment config
```

API prefixes:

- `/api/auth` — register, login
- `/api/users`
- `/api/products`
- `/api/carts`
- `/api/orders`
- `/api/income`

## Getting started

```bash
npm install
# create a .env with at least:
#   mongo_url=...
#   port_no=5000
#   PASS_SEC=...
#   SEC_KEY=...
npm start
```

Do not commit `.env` or real secrets. Adjust CORS `origin` in `index.js` for your storefront URL.

## Live

- API base: https://backend-ecommerce-plum.vercel.app
