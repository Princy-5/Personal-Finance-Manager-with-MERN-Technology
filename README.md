# Personal-Finance-Manager-with-MERN-Technology
## 1. Project Setup (Folder Structure):
```
my-finance-manager/
├── client/                # React frontend
│   ├── public/
│   ├── src/
│   │   ├── components/    # React components
│   │   ├── App.js         # Main React App file
│   │   ├── index.js       # Entry point for React app
│   │   └── styles.css     # Styling (optional)
├── server/                # Backend (Node.js/Express)
│   ├── controllers/       # Controller for API routes
│   ├── models/            # Mongoose models
│   ├── routes/            # Express routes
│   ├── server.js          # Entry point for Node.js backend
│   └── config/            # MongoDB connection and configurations
└── package.json           # Project dependencies
```
## 2. Backend Setup (Node/Express):

-1. Initialize the backend:
```
mkdir server
cd server
npm init -y
npm install express mongoose cors dotenv
```
-2.Create <b>server.js</b>:

