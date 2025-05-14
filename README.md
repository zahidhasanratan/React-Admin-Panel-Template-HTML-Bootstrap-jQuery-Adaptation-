
# Admin Panel Template – File and Folder Structure

This admin panel template is built using **HTML**, **CSS**, **Bootstrap**, **JavaScript**, and **jQuery**.

## 📁 Folder Structure

```
admin-panel-template/
│
├── index.html                 # Main dashboard page
├── README.md                  # Project documentation
│
├── css/
│   └── style.css              # Custom stylesheet
│
├── js/
│   └── script.js              # Custom JavaScript and jQuery logic
│
├── img/                       # Folder for images
│   └── (place image files here)
│
├── pages/                     # Additional pages
│   └── users.html             # Sample inner page: Users List
│
└── partials/                  # Optional common components
    ├── header.html            # Top navigation bar (optional)
    └── sidebar.html           # Sidebar navigation (optional)
```

## 📄 File Descriptions

- **index.html**: Main entry point of the admin panel dashboard.
- **css/style.css**: Contains all custom CSS styles.
- **js/script.js**: Includes all JavaScript logic and jQuery code.
- **pages/users.html**: Example of an inner page (like a user list).
- **img/**: Place all your images or icons here.
- **partials/**: Optional reusable UI components like headers, sidebars, etc.


# 🛠️ React Admin Panel Template (HTML, Bootstrap, jQuery Adaptation)

This is a simple and clean admin panel template built using **React**, adapted from a static HTML version that used **Bootstrap 5**, **CSS**, **JavaScript**, and **jQuery**.

---

## 📁 Folder Structure

```
react-admin-panel/
├── public/
│   └── index.html
├── src/
│   ├── assets/
│   │   ├── css/
│   │   │   └── style.css
│   │   └── images/
│   │       └── logo.png
│   ├── components/
│   │   ├── Sidebar.js
│   │   └── Dashboard.js
│   ├── App.js
│   ├── index.js
│   └── index.css
├── package.json
└── README.md
```

---

## 🚀 Setup Instructions

1. **Create React App:**

```bash
npx create-react-app react-admin-panel
cd react-admin-panel
```

2. **Install Bootstrap and jQuery:**

```bash
npm install bootstrap jquery
```

3. **Import Bootstrap in `index.js`:**

```js
import 'bootstrap/dist/css/bootstrap.min.css';
import 'bootstrap/dist/js/bootstrap.bundle.min.js';
import 'jquery';
```

---

## 📄 Source Code

### `src/index.js`

```js
import React from 'react';
import ReactDOM from 'react-dom/client';
import App from './App';
import './index.css';
import 'bootstrap/dist/css/bootstrap.min.css';
import 'bootstrap/dist/js/bootstrap.bundle.min.js';
import 'jquery';

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<App />);
```

---

### `src/App.js`

```jsx
import React from 'react';
import Sidebar from './components/Sidebar';
import Dashboard from './components/Dashboard';
import './assets/css/style.css';

function App() {
  return (
    <div className="d-flex" id="wrapper">
      <Sidebar />
      <div id="page-content-wrapper" className="p-4 w-100">
        <Dashboard />
      </div>
    </div>
  );
}

export default App;
```

---

### `src/components/Sidebar.js`

```jsx
import React from 'react';

function Sidebar() {
  return (
    <div className="bg-dark text-white p-3" id="sidebar-wrapper">
      <h4 className="mb-4">Admin Panel</h4>
      <div className="list-group list-group-flush">
        <a href="#" className="list-group-item list-group-item-action bg-dark text-white">Dashboard</a>
        <a href="#" className="list-group-item list-group-item-action bg-dark text-white">Users</a>
        <a href="#" className="list-group-item list-group-item-action bg-dark text-white">Settings</a>
        <a href="#" className="list-group-item list-group-item-action bg-dark text-white">Logout</a>
      </div>
    </div>
  );
}

export default Sidebar;
```

---

### `src/components/Dashboard.js`

```jsx
import React, { useEffect, useState } from 'react';

function Dashboard() {
  const [users, setUsers] = useState([]);

  useEffect(() => {
    const dummyUsers = [
      { id: 1, name: "John Doe", email: "john@example.com" },
      { id: 2, name: "Jane Smith", email: "jane@example.com" },
      { id: 3, name: "Mike Johnson", email: "mike@example.com" },
    ];
    setUsers(dummyUsers);
  }, []);

  return (
    <>
      <h2>Dashboard</h2>
      <p>Welcome to the Admin Panel!</p>
      <table className="table table-bordered mt-4">
        <thead className="table-dark">
          <tr>
            <th>ID</th>
            <th>Name</th>
            <th>Email</th>
            <th>Actions</th>
          </tr>
        </thead>
        <tbody>
          {users.map((user) =>
            <tr key={user.id}>
              <td>{user.id}</td>
              <td>{user.name}</td>
              <td>{user.email}</td>
              <td>
                <button className="btn btn-sm btn-primary me-2">Edit</button>
                <button className="btn btn-sm btn-danger">Delete</button>
              </td>
            </tr>
          )}
        </tbody>
      </table>
    </>
  );
}

export default Dashboard;
```

---

### `src/assets/css/style.css`

```css
body {
  font-family: Arial, sans-serif;
}

#wrapper {
  min-height: 100vh;
}

#sidebar-wrapper {
  min-width: 200px;
  height: 100vh;
}
```

---

## 📦 Build & Run

Start the development server:

```bash
npm start
```

---

## ✅ Features

- Bootstrap 5 layout
- Sidebar navigation
- User data displayed in table
- jQuery support (if needed later)
- Fully responsive layout

---

## 🔧 Next Improvements

- Add React Router for page navigation
- Add modals for editing users
- Connect to backend (Laravel, Express, etc.)
- Use state management (e.g., Redux)

---

