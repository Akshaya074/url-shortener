# 🔗 Distributed URL Shortener Service

A scalable URL Shortener built using Node.js, Express, and MongoDB that generates short links, handles redirection, and tracks analytics.

---

## 🚀 Overview

This project is a backend-focused URL shortening service that converts long URLs into compact short links and efficiently redirects users. It is designed with scalability and performance in mind, incorporating concepts like indexing, caching (extendable), and optimized database queries.

---

## ✨ Features

- 🔗 Short URL generation using unique identifiers  
- 🔁 Fast redirection to original URLs  
- 📊 Click analytics tracking  
- 🗑️ URL deletion functionality  
- 🗄️ Persistent storage using MongoDB  
- ⚡ Optimized queries for low-latency responses  

---

## 🏗️ System Architecture

The system follows a **client-server architecture**:

- **Client**: Sends requests (create short URL, redirect, delete)
- **Server**: Handles API logic using Express.js
- **Database**: MongoDB stores URL mappings and analytics

### 🔄 Flow

1. User submits long URL  
2. Server generates short ID  
3. Data stored in MongoDB  
4. Short URL returned to user  
5. On access → redirected to original URL  

---

## 🧠 Database Schema

Collection: `urls`

| Field   | Type   | Description |
|--------|--------|-------------|
| full   | String | Original URL |
| short  | String | Generated short ID |
| clicks | Number | Number of visits |

---

## ⚙️ Tech Stack

- **Backend**: Node.js, Express.js  
- **Database**: MongoDB, Mongoose  
- **Templating**: EJS  
- **Styling**: Bootstrap  

---

## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/YOUR_USERNAME/url-shortener.git
cd url-shortener
2. Install dependencies
npm install
3. Setup environment variables

Create a .env file:

MONGO_URI=mongodb://localhost:27017/url-shortener
PORT=5000
4. Run the application
npm start

Open:

http://localhost:5000
