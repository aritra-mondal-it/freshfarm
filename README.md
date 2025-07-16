# 🥦 Fresh Frame - Grocery Ordering Website

Fresh Frame is a modern and responsive grocery ordering platform built with the **MERN Stack** (MongoDB, Express, React, Node.js). It allows users to browse groceries, add them to a cart, and securely purchase using **Stripe**. Product images are stored and managed with **Cloudinary**, and the entire application is deployed on **Vercel** for fast and scalable delivery.

---

## 🚀 Features

- 🛒 Browse a wide range of grocery items
- 🧺 Add to cart and manage quantities
- 💳 Secure payments via Stripe
- 🖼 Image upload and management using Cloudinary (for sellers/admin)
- 🔐 User authentication and order history
- 📦 Admin dashboard for managing inventory
- 🌐 Fully deployed with Vercel

---

## 🛠️ Tech Stack

**Frontend**
- React
- Axios
- Tailwind CSS

**Backend**
- Node.js
- Express.js
- MongoDB (Mongoose)
- Cloudinary (image uploads)
- Stripe (payment integration)
- JWT (authentication)

**Deployment**
- Vercel

---

## ⚙️ Installation & Setup

### 📂 Clone the Repository

```bash
git clone https://github.com/yourusername/freshfarm.git
cd freshfarm
```

---

## 🧑‍💻 First Run — Server Then Client

---

### ❖ Setup the Server

1. Open the project folder in **VS Code**

2. Create a **MongoDB Atlas** account and get your connection string  
👉 https://www.mongodb.com/cloud/atlas/register

3. Create a **Cloudinary** account  
👉 https://cloudinary.com/users/register_free

4. Create a `.env` file inside the `/server` folder and add:

```env
MONGO_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret
STRIPE_SECRET_KEY=your_stripe_secret_key
```

5. Open the server folder and run:

```bash
cd server
npm install
npm run server
```

🔗 This will start your backend at: `http://localhost:5000`

---

### ❖ Setup the Client

1. Create a `.env` file inside the `/client` folder and add:

```env
REACT_APP_STRIPE_PUBLISHABLE_KEY=your_stripe_publishable_key
```

2. Open the client folder and run:

```bash
cd client
npm install
npm run dev
```

🔗 This will start your frontend at: `http://localhost:3000`

---

## 💳 (Optional) Stripe Online Payment Setup & Deployment

---

### 1. Create Stripe Account  
👉 https://dashboard.stripe.com/login

- Get your **Stripe Secret Key** and **Publishable Key**
- Add them to your `.env` files

---

### 2. Push Project to GitHub  
Upload your entire project to GitHub for deployment.

---

### 3. Deploy Backend on Vercel  
👉 https://vercel.com/

- Import the `/server` folder as a separate Vercel project
- In Vercel dashboard, add the same environment variables from `.env`
- Make sure to include:

```env
NODE_ENV=production
```

---

### 4. Setup Stripe Webhooks (for payment confirmation)

- Go to: **Stripe > Developers > Webhooks**
- Add your backend webhook endpoint, e.g.:

```
https://your-backend.vercel.app/api/webhook
```

- Copy the **Stripe Webhook Signing Secret** and add it to `.env`:

```env
STRIPE_WEBHOOK_SECRET=your_webhook_signing_key
```

---

### 5. Deploy Frontend on Vercel

- Import and deploy the `/client` folder on Vercel
- In your `server.js`, update CORS settings:

```js
origin: "https://fresh-frame.vercel.app"
```

- Redeploy the backend to apply the new CORS configuration

---

## 💳 Stripe Test Card (For Testing Payments)

Use the following test card to simulate successful Stripe payments:

```yaml
Card Number: 6969 6969 6969 6969
Expiry: Any future date
CVC: Any 3 digits
ZIP: Any 5-digit number
```

## 🤝 Contributing

Pull requests are welcome. For major changes, open an issue first to discuss your ideas.

---

## 📄 License

This project is licensed under the MIT License.

---

## 👨‍💻 Author

**Your Name**  
🔗 [GitHub](https://github.com/aritra-mondal-it)
