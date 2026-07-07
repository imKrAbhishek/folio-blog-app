# Folio. | Full-Stack MERN Blog ✍️

A modern, full-stack blogging platform built with the MERN stack (MongoDB, Express, React, Node.js). Folio allows users to read articles, register for accounts, and features a robust Role-Based Access Control (RBAC) system that empowers 'Authors' to write, format, and publish stories using a rich-text editor.

## ✨ Key Features

* **Secure Authentication:** Utilizes HTTP-only cookies and JSON Web Tokens (JWT) to keep user sessions secure and persistent against XSS attacks.
* **Role-Based Access Control (RBAC):** Protects routes and UI elements. 'Readers' can browse articles, while 'Authors' get access to a private dashboard and writing tools.
* **Rich Text Editing:** Integrated with `react-quill` to allow authors to format their posts, add links, and structure their content beautifully.
* **Dynamic Avatars:** Automatically generates customized fallback avatars using user initials via the UI-Avatars API if a profile picture is missing.
* **Robust Validation:** Backend API routes are strictly protected and validated using `Zod` to prevent bad data from reaching the database.
* **Responsive UI:** A premium, medium-style reading layout built from the ground up using Tailwind CSS and Vite.

## 🛠️ Tech Stack

**Frontend:**
* React (Vite)
* Tailwind CSS & Tailwind Typography
* React Router v6
* Axios (configured for cross-origin credentials)
* React-Quill

**Backend:**
* Node.js & Express
* MongoDB & Mongoose
* JSON Web Tokens (JWT) & bcryptjs
* Zod (Schema Validation)
* Cookie-Parser & CORS

## 🚀 Getting Started

Follow these instructions to get a copy of the project up and running on your local machine for development and testing.

### Prerequisites
* [Node.js](https://nodejs.org/) installed on your machine.
* A running instance of [MongoDB](https://www.mongodb.com/) (Local or Atlas).

### Installation

**1. Clone the repository:**
\`\`\`bash
git clone https://github.com/YOUR_USERNAME/folio-blog-app.git
cd folio-blog-app
\`\`\`

**2. Setup the Backend:**
\`\`\`bash
cd blog-backend
npm install
\`\`\`
Create a `.env` file in the `blog-backend` directory and add the following:
\`\`\`env
PORT=5000
MONGODB_URI=mongodb://127.0.0.1:27017/blog_db
JWT_SECRET=your_super_secret_jwt_key_here
NODE_ENV=development
\`\`\`
Start the backend server:
\`\`\`bash
npm run dev
\`\`\`

**3. Setup the Frontend:**
Open a new terminal window and navigate to the frontend directory:
\`\`\`bash
cd blog-frontend
npm install
\`\`\`
*(Optional)* Create a `.env` file in the `blog-frontend` directory if your API is hosted elsewhere:
\`\`\`env
VITE_API_BASE_URL=http://localhost:5000/api
\`\`\`
Start the frontend development server:
\`\`\`bash
npm run dev
\`\`\`

## 📝 Usage / Testing Notes
* By default, new users register as a **Reader**. 
* To test the authoring features, you can temporarily change the default role in `models/User.js` to `author`, or manually update your user document in MongoDB Compass.
* Once logged in as an author, click **Write a Story** to test the rich-text editor and Zod validation.

---
*Designed and built by Abhishek Kumar.*
