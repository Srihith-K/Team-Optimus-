# 🎓 Proctor Hack

Proctor Hack is a real-time monitoring backend system designed for
online exams.

It receives suspicious activity alerts (such as tab switching or unusual
behavior) from a Chrome extension and instantly forwards them to a
Teacher Control Panel using WebSockets.

------------------------------------------------------------------------

## 🚀 Features

-   Real-time risk monitoring
-   WebSocket-based live alerts
-   REST API endpoint for logging risks
-   Simple teacher dashboard interface
-   Lightweight Node.js backend

------------------------------------------------------------------------

## 🛠 Tech Stack

-   Node.js
-   Express.js
-   Socket.io
-   CORS

------------------------------------------------------------------------

## 📂 Project Structure

    proctor-hack/
    │
    ├── server.js
    ├── teacher-control-panel.html
    ├── package.json
    ├── package-lock.json
    └── README.md

------------------------------------------------------------------------

## 📦 Requirements

Make sure you have installed:

-   Node.js (v16+ recommended)
-   npm (comes with Node.js)

Check installation:

    node -v
    npm -v

------------------------------------------------------------------------

## ⚙️ Installation

### 1️⃣ Clone the Repository

    git clone https://github.com/YOUR-USERNAME/proctor-hack.git
    cd proctor-hack

### 2️⃣ Install Dependencies

    npm install

------------------------------------------------------------------------

## ▶️ Run the Server

Start the backend server:

    node server.js

If successful, you should see:

    Server running on http://localhost:5000

------------------------------------------------------------------------

## 🌐 Using the Teacher Control Panel

1.  Make sure the server is running.
2.  Open the file:

```{=html}
<!-- -->
```
    teacher-control-panel.html

in your browser.

The dashboard will automatically connect to the backend and display live
alerts.

------------------------------------------------------------------------

## 🔌 API Endpoint

### POST `/log-risk`

Example request:

``` json
POST http://localhost:5000/log-risk
Content-Type: application/json

{
  "student": "John Doe",
  "riskLevel": "High",
  "reason": "Tab switching detected"
}
```

When the server receives this: - The event is logged - A real-time alert
is pushed to the teacher dashboard via Socket.io

------------------------------------------------------------------------

## 📜 License

ISC License
