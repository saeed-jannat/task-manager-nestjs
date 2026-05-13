

📋 Task Manager API - NestJS

A scalable and real-time Task Manager backend built with NestJS, using Redis for caching and queue management, Socket.IO for realtime updates, and JWT authentication for secure access control.
🚀 Features

    🔐 JWT Authentication & Authorization

    👤 User Registration & Login

    📋 Create, Update, Delete Tasks

    ✅ Task Status Management

    ⚡ Real-time task updates with Socket.IO

    🚀 Redis caching & pub/sub support

    🧩 Modular architecture with NestJS

    🗄️ Database ORM support (Prisma / TypeORM)

    🛡️ Validation & Error Handling

    📡 RESTful API

    🧪 Unit & E2E Testing support

    📄 Swagger API Documentation

🏗️ Tech Stack
Technology	Purpose
NestJS	Backend Framework
Redis	Cache / Pub-Sub
Socket.IO	Realtime Events
JWT	Authentication
Passport	Auth Strategy
PostgreSQL / MySQL	Database
Prisma / TypeORM	ORM
Docker	Containerization
📂 Project Structure

src/
│
├── auth/
├── users/
├── tasks/
├── sockets/
├── redis/
├── common/
├── config/
│
├── app.module.ts
└── main.ts

🔐 Authentication

This project uses JWT-based authentication.
Flow

    User registers

    User logs in

    Server generates JWT token

    Client sends token in Authorization header

Authorization: Bearer YOUR_TOKEN

⚡ Real-time Updates

Using Socket.IO, users receive live task updates:

    Task Created

    Task Updated

    Task Deleted

    Task Status Changed

Example event:

socket.emit("task:update", {
  id: 1,
  title: "Update README",
  status: "DONE"
});

🚀 Redis Usage

Redis is used for:

    Caching

    Session storage

    Pub/Sub messaging

    Rate limiting

    WebSocket scaling

🛠️ Installation
Clone Repository

git clone https://github.com/saeed-jannat/task-manager-api.git

Enter Project

cd task-manager-api

Install Dependencies

npm install

⚙️ Environment Variables

Create a .env file:

PORT=3000

DATABASE_URL=postgresql://user:password@localhost:5432/task_manager

JWT_SECRET=your_secret_key

REDIS_HOST=localhost
REDIS_PORT=6379

▶️ Run Project
Development

npm run start:dev

Production

npm run build
npm run start:prod

🐳 Docker Support

docker-compose up --build

📡 API Endpoints
Auth
Method	Endpoint	Description
POST	/auth/register	Register user
POST	/auth/login	Login user
Tasks
Method	Endpoint
GET	/tasks
POST	/tasks
PATCH	/tasks/:id
DELETE	/tasks/:id
📄 Swagger Documentation

Swagger documentation available at:

http://localhost:3000/api

🧪 Testing
Unit Tests

npm run test

E2E Tests

npm run test:e2e

🔮 Future Improvements

    Task labels & categories

    Team collaboration

    File attachments

    Notifications system

    Activity logs

    Microservices architecture

    Kubernetes deployment

🤝 Contributing

Pull requests are welcome.

    Fork the project

    Create your feature branch

    Commit your changes

    Push to the branch

    Open a Pull Request

📜 License

MIT License
⭐ Support

If you like this project, give it a star on GitHub ⭐


