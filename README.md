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

* 1. Initialize the backend:
```
mkdir server
cd server
npm init -y
npm install express mongoose cors dotenv
```
* 2.Create <b>server.js</b>:
  
```
const express = require("express");
const cors = require("cors");
const mongoose = require("mongoose");
require("dotenv").config();

const app = express();
const port = process.env.PORT || 5000;
app.use(cors());
app.use(express.json());
mongoose.connect(process.env.MONGO_URI, { useNewUrlParser: true, useUnifiedTopology: true })
  .then(() => console.log('MongoDB connected'))
  .catch((err) => console.log(err));
app.get("/", (req, res) => {
  res.send("Welcome to Personal Finance Manager API");
});
app.listen(port, () => {
  console.log(`Server is running on port: ${port}`);
});
```
* 3.Create .env for environment variables:

```
 MONGO_URI=your_mongodb_connection_string
```
## 3. Frontend Setup (React):

* Create React app:
```
  npx create-react-app client
  cd client
  npm start
```




