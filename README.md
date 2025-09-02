# FarmConnect

FarmConnect is a **web-based marketplace** connecting farmers directly with buyers.  
Farmers can manage products and orders, while buyers can shop, pay securely, and get AI-generated recipe suggestions.

---

## Table of Contents
1. [Project Overview](#project-overview)
2. [Features](#features)
3. [Tech Stack](#tech-stack)
4. [User Flow](#user-flow)
5. [Architecture](#architecture)
6. [Future Enhancements](#future-enhancements)

---

## Project Overview

FarmConnect bridges the gap between farmers and buyers, providing:

- **Farmers:** Dashboard to manage products and view orders.
- **Buyers:** Marketplace to browse products, add to cart, make payments, and view order history.
- **Common:** Secure authentication, profile management, and recommendations.

---

## Features

### Farmers
- Add, edit, delete products with images, prices, and categories.
- View customer orders and update status (pending → paid → delivered).
- Manage inventory via a responsive dashboard.

### Buyers
- Browse products with AI-powered recommendations.
- Add to cart, adjust quantities, and remove items.
- Secure payments via IntaSend.
- View order history and order status.
- AI-generated recipe suggestions based on cart items.

### General
- User authentication with Supabase Auth.
- Supabase Storage for images.
- Responsive design with TailwindCSS.

---

## Tech Stack
- **Frontend:** HTML, Tailwind CSS, JavaScript
- **Backend & Database:** Supabase (Auth, Database, Storage)
- **Payment Gateway:** IntaSend Inline JS SDK

---

## User Flow
flowchart TD
    A[Visit Website] --> B{Logged In?}
    B -- No --> C[Login / Signup]
    B -- Yes --> D{User Role}
    D -- Farmer --> E[Dashboard]
    E --> F[Manage Products]
    E --> G[View Orders]
    D -- Buyer --> H[Marketplace]
    H --> I[Add to Cart]
    I --> J[Checkout / IntaSend Payment]
    J --> K[Order History]

## Architecture
graph LR
    subgraph Frontend
        A[HTML / CSS / JS Pages] --> B[Dashboard / Marketplace / Cart / Orders / Profile]
    end
    subgraph Backend
        C[Supabase DB] --> D[Tables: Products, Orders, Profiles]
        E[Supabase Auth] --> D
        F[Supabase Storage] --> B
    end
    B --> C
    B --> E
    B --> F
    G[IntaSend Payment Gateway] --> B
    
## Future Enhancements

  1. Advanced product search and filtering.

  2. Sales analytics dashboard for farmers.

  3. Product reviews and ratings.

  4. Real-time notifications for orders.

  5. More advanced AI recipe suggestions.

    

    
