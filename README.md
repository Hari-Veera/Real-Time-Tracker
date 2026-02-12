markdown
# Real-Time-Tracker

A high-performance, reliable backend system for real-time location tracking using **Socket.IO**, **Express**, and **EJS**. This backend handles live location updates, stores historical tracking data, and provides secure APIs for frontend or client applications to fetch current and past positions.

This system can be used in logistics tracking, fleet monitoring,
delivery tracking, or real-time asset management applications.


---

## Features

- **Real-Time Location Updates**: Receive and broadcast live location data using Socket.IO.
- **Historical Tracking**: Store and query past location data efficiently.
- **Server-Rendered Frontend**: EJS templates for dashboards and visualization.
- **Secure APIs**: RESTful endpoints with authentication support.
- **Scalable Architecture**: Optimized for low-latency responses and multiple concurrent clients.
- **Data Integrity**: Reliable storage and retrieval of location information.
- Event-driven architecture using WebSockets
- Optimized broadcast mechanism for multiple clients


---

## Tech Stack

- **Backend**: Node.js with Express
- **Real-Time Communication**: Socket.IO
- **Frontend Templating**: EJS
- Database: MongoDB (Mongoose ODM)
- **Authentication**: JWT
- **Containerization**: Docker *(optional)*

---

## Installation

1. Clone the repository:

```
bash
git clone https://github.com/Hari-Veera/Real-Time-Tracker.git
cd realtime-tracking-backend
```

2. Install dependencies:

```
bash
npm install
```

3. Configure environment variables:

```
env
DATABASE_URL=your_database_url
JWT_SECRET=your_jwt_secret
PORT=4000
```

4. Start the server:

```
bash
npm start
```

---

### Authentication

- \`POST /api/auth/login\` – User login
- \`POST /api/auth/register\` – User registration

### Location Tracking

- \`POST /api/locations\` – Submit current location
- \`GET /api/locations/current\` – Fetch current location
- \`GET /api/locations/history?userId=<id>\` – Fetch historical locations

> All endpoints require authentication via JWT.

### Sample Response

```
{
  "userId": "123",
  "latitude": 17.3850,
  "longitude": 78.4867,
  "timestamp": "2026-02-10T12:30:00Z"
}
```

---

## Architecture Diagram

```
Client App (Web/Mobile)
        |
        | Socket.IO / REST API
        v
Express + Socket.IO Backend
        |
        | Authentication & Validation
        v
EJS Frontend / Analytics
```

---

## Live Demo

🔗 [https://your-live-url.com](https://real-time-tracker-807v.onrender.com/)


## Author

Medipudi Hari Veera  
GitHub: https://github.com/Hari-Veera  
Email: hariveeramedipudi@gmail.com


## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

---
