# Demo E-Commerce

E-commerce storefront demo built with Next.js, Apollo GraphQL and Redux Toolkit, using the public Platzi Fake Store GraphQL API.

**Live demo:** https://demo-ecommerce-sooty.vercel.app/

## Features

- Product listing fetched via GraphQL (`https://api.escuelajs.co/graphql`)
- Product detail pages (`/products/[id]`) with image display, size/color variation controls, quantity control and reviews
- Shopping cart (Redux slice) with cart page and sidebar
- Checkout and thank-you pages
- Login and sign-up pages using the API's GraphQL auth mutations

## Tech Stack

Next.js (App Router) · TypeScript · React · Apollo Client · GraphQL · Redux Toolkit · React Redux · Tailwind CSS

## Project Structure

```
src/
  app/          # /, products/[id], cart, checkout, thank-you, auth/login, auth/signup
  components/   # NavBar, SideBar, Cart, ShowImage, VariationControl, QuantityControl, ProductReview
  graphql/      # apolloClient, getProducts query
  redux/        # store, authSlice, cartSlice, productSlice
  lib/          # authService, parseImageUrl
```

## Getting Started

```bash
git clone https://github.com/mohammed-samiul-islam/demo-ecommerce.git
cd demo-ecommerce
npm install
npm run dev
```

Open http://localhost:3000. Other scripts: `npm run build`, `npm run start`, `npm run lint`.

No environment variables are required.

## Design Notes

Component-based architecture; global state (auth, cart, products) managed with Redux Toolkit; remote data via Apollo Client with an in-memory cache.
