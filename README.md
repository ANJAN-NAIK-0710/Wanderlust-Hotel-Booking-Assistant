# 🌍 Wanderlust — AI Hotel Booking Assistant

> **Your Digital Concierge for Extraordinary Stays**

Wanderlust is an **AI-powered hotel booking assistant** designed to make discovering and booking hotels easier through an intelligent conversational experience.

🔗 **Live Demo:** https://wanderlust-hotel-booking-assistant-1.onrender.com/

---

## ✨ Features

* 🤖 **AI-Powered Hotel Assistant** — conversational assistance for hotel discovery
* 🏨 **Hotel Discovery & Booking** — browse hotels and complete bookings
* 🔐 **User Authentication** — secure registration and login
* 💳 **Online Payments** — integrated Razorpay payment processing
* 📧 **Email Notifications** — booking-related transactional emails
* 🎨 **Modern Responsive UI** — clean, travel-focused interface
* 🗄️ **MongoDB Database** — stores users, hotels, bookings, and application data

---

## 🧠 How Wanderlust Works

```text
                    ┌─────────────────────┐
                    │       User          │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   Wanderlust UI     │
                    │    Web Application  │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   AI Concierge      │
                    │     OpenAI API      │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Hotel Search &      │
                    │ Recommendations     │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Hotel Selection     │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │      Booking        │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Razorpay Payment    │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Booking Confirmation│
                    │    + Email          │
                    └─────────────────────┘
```

---

## 🛠️ Tech Stack

### Frontend

* React.js
* JavaScript
* HTML5
* CSS3

### Backend

* Node.js
* Express.js
* REST APIs

### AI

* OpenAI API
* Natural-language conversational assistant
* AI-powered hotel recommendations

### Database

* **MongoDB**
* MongoDB Atlas
* Mongoose ODM

### Payments

* Razorpay

### Email

* Resend

### Deployment

* Render

---

## 🏗️ System Architecture

```text
                    ┌──────────────────────┐
                    │      Frontend        │
                    │       React.js       │
                    └──────────┬───────────┘
                               │
                         HTTP / REST API
                               │
                               ▼
                    ┌──────────────────────┐
                    │       Backend        │
                    │  Node.js + Express   │
                    └──────────┬───────────┘
                               │
            ┌──────────────────┼──────────────────┐
            │                  │                  │
            ▼                  ▼                  ▼
     ┌─────────────┐    ┌─────────────┐    ┌─────────────┐
     │   OpenAI    │    │   MongoDB   │    │  Razorpay   │
     │     AI      │    │   Database  │    │   Payments  │
     └─────────────┘    └─────────────┘    └─────────────┘
                               │
                               ▼
                       ┌─────────────┐
                       │   Resend    │
                       │    Email    │
                       └─────────────┘
```

---

## 🗄️ Database

Wanderlust uses **MongoDB** as its primary database.

MongoDB provides a flexible document-oriented structure suitable for managing the application's users, hotels, bookings, and related information.

Typical collections include:

```text
MongoDB
│
├── Users
│   ├── User details
│   ├── Authentication information
│   └── Account data
│
├── Hotels
│   ├── Hotel information
│   ├── Location
│   ├── Pricing
│   └── Availability
│
└── Bookings
    ├── User information
    ├── Hotel information
    ├── Booking details
    ├── Payment information
    └── Booking status
```

---

## 🔑 Environment Variables

Create a `.env` file in the backend:

```env
OPENAI_API_KEY=your_openai_api_key

MONGODB_URI=your_mongodb_connection_string

RAZORPAY_KEY_ID=your_razorpay_key_id
RAZORPAY_KEY_SECRET=your_razorpay_key_secret
RAZORPAY_WEBHOOK_SECRET=your_razorpay_webhook_secret

RESEND_API_KEY=your_resend_api_key
RESEND_FROM_EMAIL=your_email
```

> ⚠️ Never commit `.env` files or API keys to GitHub.

Add:

```gitignore
.env
.env.local
node_modules/
```

---

## 🚀 Getting Started

### Prerequisites

Make sure you have:

* Node.js
* npm
* Git
* MongoDB / MongoDB Atlas account
* OpenAI API key
* Razorpay account
* Resend account

### Clone the Repository

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>

cd Wanderlust
```

### Install Dependencies

Frontend:

```bash
cd frontend
npm install
```

Backend:

```bash
cd ../backend
npm install
```

### Run the Application

Start the backend:

```bash
cd backend
npm run dev
```

Start the frontend in another terminal:

```bash
cd frontend
npm run dev
```

---

## 💳 Payment Flow

Wanderlust uses Razorpay for payment processing.

```text
User selects hotel
       ↓
Booking details entered
       ↓
Razorpay payment initiated
       ↓
Payment completed
       ↓
Payment verified by backend
       ↓
Booking stored in MongoDB
       ↓
Confirmation email sent
```

---

## 📧 Email Flow

Resend is used for transactional email communication.

```text
Booking completed
       ↓
Backend processes booking
       ↓
Booking saved in MongoDB
       ↓
Confirmation generated
       ↓
Email sent through Resend
```

---

## ☁️ Deployment

The application is deployed using **Render**.

### Live Application

https://wanderlust-hotel-booking-assistant-1.onrender.com/

---

## 🔒 Security

The application follows standard security practices including:

* Environment variables for sensitive credentials
* Protected API keys
* Secure authentication
* Server-side payment verification
* Razorpay webhook verification
* Backend input validation
* Secure MongoDB connection

---

## 🎯 Project Objective

Wanderlust aims to combine **traditional hotel booking with AI-powered conversational assistance**.

Instead of navigating through multiple filters, users can describe their requirements naturally:

```text
"I need a luxury hotel in Goa for 3 nights."
```

The AI assistant can then help guide the user toward suitable accommodation options and the booking process.

---

## 🌟 Why Wanderlust?

### Traditional Booking

```text
Search
  ↓
Filter
  ↓
Compare
  ↓
View Hotels
  ↓
Select Hotel
  ↓
Book
  ↓
Pay
```

### Wanderlust

```text
Tell the AI what you need
          ↓
AI understands your requirements
          ↓
Discover suitable hotels
          ↓
Select
          ↓
Book
          ↓
Pay
```

The goal is to make hotel discovery **more conversational, personalized, and intuitive**.

---

## 👨‍💻 Author

**Anjan**

A full-stack AI-powered hotel booking project combining:

**AI + React + Node.js + Express + MongoDB + Payments + Email + Cloud Deployment**

---

## 📄 License

This project is intended for educational and portfolio purposes.

---

### 🌍 Wanderlust

**Your Digital Concierge for Extraordinary Stays.**
