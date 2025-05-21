# 🏆 Sports Updates Portal

A **modern, real-time sports news and updates platform** powered by cutting-edge technologies.

[![MIT License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
![Node.js](https://img.shields.io/badge/Backend-Node.js-green)
![React](https://img.shields.io/badge/Frontend-React-blue)
![MongoDB](https://img.shields.io/badge/Database-MongoDB-brightgreen)

---

## 🌐 Live Features

✅ Real-time news  
✅ Live scores & statistics  
✅ Authentication & profiles  
✅ Admin dashboard  
✅ Mobile responsive  
✅ API integration  

---

## 🧰 Tech Stack

### 🖥️ Frontend
> Built with **React**, styled with **Tailwind CSS**, and animated using **Framer Motion**.

- ⚛️ **React.js**
- 🧠 **TypeScript**
- 🎨 **Tailwind CSS**
- 🔁 **React Router**
- 📦 **Axios**
- ⚡ **React Query**
- 🎞 **Framer Motion**

### 🛠️ Backend
> Built with **Node.js**, secured with **JWT**, and powered by **MongoDB**.

- 🚀 **Node.js**, **Express.js**
- 🧠 **TypeScript**
- 🛢️ **MongoDB**, **Mongoose**
- 🔐 **JWT**, **Bcrypt**
- 🌐 **CORS**, **Dotenv**

### ⚙️ Dev Tools
- 🧹 **ESLint**, **Prettier**
- 🔁 **Nodemon**, **Concurrently**
- 📦 **TypeScript**

---

## 🎯 Key Features

### 👤 User
- 📰 Real-time sports news
- 📺 Live match scores & statistics
- 📊 Player & team analytics
- 🔍 Smart search
- 🔔 Notifications
- 💬 Commenting system

### 🛡️ Admin
- 📝 CMS for content updates
- 📈 Analytics dashboard
- 👥 Manage users
- ⚙️ System configuration
- 🔍 Performance monitoring

---

## 🏗️ System Architecture

```mermaid
flowchart TD
  subgraph UI["🖥️ Frontend"]
    A1[🎨 UI Components]
    A2[🔄 State Management]
    A3[🛣️ React Router]
    A4[📡 API Client]
    A5[🔐 Authentication]
    A6[💅 Styling]
  end

  subgraph Server["🔧 Backend"]
    B1[🎮 Controllers]
    B2[⚙️ Services]
    B3[🔒 Auth Service]
    B4[💾 Cache Layer]
    B5[✅ Validation]
    B6[📊 Data Models]
  end

  subgraph DB["🗄️ Database"]
    C1[📚 Collections]
    C2[🔍 Indexes]
    C3[⚡ Redis Cache]
    C4[💿 Backups]
  end

  subgraph External["🌍 External Services"]
    D1[🏆 Sports API]
    D2[📰 News API]
    D3[☁️ CDN Storage]
  end

  %% Frontend connections
  A1 --> A2
  A2 --> A3
  A3 --> A4
  A4 --> A5
  A5 --> A6

  %% Backend connections
  A4 --> B1
  B1 --> B2
  B2 --> B3
  B2 --> B6
  B2 --> B4
  B3 --> B5

  %% Database connections
  B6 --> C1
  C1 --> C2
  B4 --> C3
  C3 --> C4

  %% External connections
  B2 --> D1
  B2 --> D2
  A1 --> D3

  %% Styling
  classDef frontend fill:#4F46E5,stroke:#312E81,stroke-width:2px,color:white,font-weight:bold
  classDef backend fill:#059669,stroke:#065F46,stroke-width:2px,color:white,font-weight:bold
  classDef database fill:#DC2626,stroke:#991B1B,stroke-width:2px,color:white,font-weight:bold
  classDef external fill:#7C3AED,stroke:#5B21B6,stroke-width:2px,color:white,font-weight:bold
  classDef component fill:#60A5FA,stroke:#1E40AF,stroke-width:1px,color:white
  classDef service fill:#34D399,stroke:#065F46,stroke-width:1px,color:white
  classDef data fill:#F87171,stroke:#991B1B,stroke-width:1px,color:white

  %% Apply styles
  class UI frontend
  class Server backend
  class DB database
  class External external
  class A1,A2,A3,A4,A5,A6 component
  class B1,B2,B3,B4,B5,B6 service
  class C1,C2,C3,C4 data
  class D1,D2,D3 external
```

> **Flow**: Frontend sends requests ➜ Backend processes via services ➜ Database fetch ➜ Data returned ➜ UI update

---

## 🏃‍♂️ Getting Started

### Prerequisites
- Docker and Docker Compose
- Node.js (v14 or higher)
- npm or yarn

### Running with Docker (Recommended)

1. Clone the repository:
```bash
git clone https://github.com/MalikShoaibAhmadKhan/sports-app.git
cd sports-app
```

2. Start all services using Docker Compose:
```bash
docker-compose up -d
```

This will start:
- Frontend at http://localhost:3001
- Backend at http://localhost:5002
- MongoDB at mongodb://localhost:27017

3. To view logs:
```bash
# View all logs
docker-compose logs -f

# View specific service logs
docker-compose logs -f server
docker-compose logs -f client
docker-compose logs -f mongodb
```

4. To stop services:
```bash
docker-compose down
```

### Running Locally (Without Docker)

1. Install dependencies:
```bash
# Install server dependencies
cd server
npm install

# Install client dependencies
cd ../client
npm install
```

2. Set up environment variables:
```bash
# In server directory
cp .env.example .env
```

3. Start MongoDB:
```bash
# If you have MongoDB installed locally
mongod

# Or use MongoDB Atlas connection string in .env file
```

4. Start the services:
```bash
# Start server (in server directory)
npm run dev

# Start client (in client directory)
npm start
```

## 📁 Project Structure

```
sports-updates/
├── client/                 # Frontend React application
│   ├── src/
│   │   ├── components/    # React components
│   │   ├── pages/        # Page components
│   │   ├── services/     # API services
│   │   └── utils/        # Utility functions
│   ├── Dockerfile        # Frontend Docker configuration
│   └── package.json
├── server/                # Backend Node.js application
│   ├── src/
│   │   ├── controllers/  # Route controllers
│   │   ├── models/       # Database models
│   │   ├── routes/       # API routes
│   │   └── services/     # Business logic
│   ├── Dockerfile        # Backend Docker configuration
│   └── package.json
├── docker-compose.yml     # Docker services configuration
└── README.md
```

## 🔧 Environment Variables

### Server (.env)
```
PORT=5002
MONGODB_URI=mongodb://admin:password123@mongodb:27017/sports-updates?authSource=admin
CLIENT_URL=http://localhost:3001
JWT_SECRET=your_jwt_secret_key_here
```

### Docker Environment
The following services are configured in docker-compose.yml:
- **MongoDB**: Database service
  - Port: 27017
  - Username: admin
  - Password: password123
  - Persistent volume: mongodb_data

- **Server**: Backend service
  - Port: 5002
  - Environment: development
  - Connected to MongoDB service

- **Client**: Frontend service
  - Port: 3001
  - Environment: development
  - Connected to Server service


---

## 🤝 Contributing

```bash
git checkout -b feature/myFeature
git commit -m "Add myFeature"
git push origin feature/myFeature
```

📬 Pull Requests are welcome!

---

## 📜 License

Licensed under the MIT License. See [`LICENSE`](./LICENSE) for more details.

---

## 👨‍💻 Author

**Your Name** — [GitHub](https://github.com/yourusername)

---

## 🙏 Acknowledgements

* Inspired by ESPN, LiveScore, and other sports platforms
* Built with ❤️ using modern tech 
