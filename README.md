# 🛒 E-Commerce Marketplace

A modern **multi-vendor e-commerce marketplace** built with **Next.js 15**, **TailwindCSS**, and a hybrid backend using **Supabase (serverless)** + **PostgreSQL**.  
This platform allows **any user to register as a seller** and manage their own store while buyers can browse, purchase, and review products seamlessly.  

---

## 🚀 Features

### 👤 User
- Sign up / Sign in with **Clerk** authentication (email, social logins)
- Browse products with search and filters
- Add products to cart and checkout securely
- Leave ratings and reviews
- Receive real-time order notifications

### 🛍 Sellers
- Seller onboarding & profile setup
- Add, edit, and delete products with variants
- Manage orders and track sales
- Dashboard with analytics
- Secure payouts via **Stripe Connect**

### 🛠 Admin
- Approve or suspend sellers
- Manage product listings
- View platform analytics (sales, top sellers, categories)
- Resolve disputes and refunds

---

## 🏗 Tech Stack

- **Frontend**: Next.js 15, TailwindCSS, shadcn/ui, React Query
- **Backend**: Supabase (Realtime API, Auth), PostgreSQL (direct queries)
- **Auth**: Clerk
- **Payments**: Stripe Connect
- **Storage**: Supabase Storage (product images, KYC docs)
- **Deploy**: Vercel (frontend) + Supabase (backend)

---

## ⚙️ Installation

Clone the repo:
```bash
git clone https://github.com/JomariTheAnalyst/ecommerce.git
cd ecommerce
