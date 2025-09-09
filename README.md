

1. Frontend (App.js)
```jsx
import React from 'react';
import { BrowserRouter, Routes, Route } from 'react-router-dom';
import Login from './components/Login';
import Dashboard from './components/Dashboard';
import MemberRegistration from './components/MemberRegistration';

function App() {
  return (
    <BrowserRouter>
      <Routes>
        <Route path="/login" element={<Login />} />
        <Route path="/dashboard" element={<Dashboard />} />
        <Route path="/register" element={<MemberRegistration />} />
      </Routes>
    </BrowserRouter>
  );
}

export default App;
```

2. Backend (server.js)
```javascript
const express = require('express');
const mongoose = require('mongoose');
const cors = require('cors');
require('dotenv').config();

const app = express();
const PORT = process.env.PORT || 5000;

app.use(cors());
app.use(express.json());

mongoose.connect(process.env.MONGODB_URI, {
  useNewUrlParser: true,
  useUnifiedTopology: true
});

// Authentication Routes
app.post('/api/login', (req, res) => {
  // Login logic
});

app.post('/api/register', (req, res) => {
  // Member registration logic
});

app.listen(PORT, () => {
  console.log(`Server running on port ${PORT}`);
});
```

3. Login Component
```jsx
import React, { useState } from 'react';

function Login() {
  const [username, setUsername] = useState('');
  const [password, setPassword] = useState('');

  const handleLogin = async (e) => {
    e.preventDefault();
    // Login authentication logic
  };

  return (
    <div>
      <h2>Miami Marlins Management Login</h2>
      <form onSubmit={handleLogin}>
        <input 
          type="text" 
          placeholder="Username" 
          value={username}
          onChange={(e) => setUsername(e.target.value)}
        />
        <input 
          type="password" 
          placeholder="Password" 
          value={password}
          onChange={(e) => setPassword(e.target.value)}
        />
        <button type="submit">Login</button>
      </form>
    </div>
  );
}

export default Login;
```

4. Package.json
```json
{
  "name": "miami-marlins-management",
  "version": "1.0.0",
  "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "server": "node server.js",
    "dev": "concurrently \"npm run start\" \"npm run server\""
  },
  "dependencies": {
    "react": "^17.0.2",
    "react-dom": "^17.0.2",
    "react-router-dom": "^6.0.0",
    "express": "^4.17.1",
    "mongoose": "^6.0.0",
    "cors": "^2.8.5",
    "dotenv": "^10.0.0"
  }
}
```

5. .env Configuration
```
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
PORT=5000
```
