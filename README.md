# Chatbot Platform

## Live Demo
https://chatbot-platform-demo.railway.app

---

## Prerequisites
- Node.js v16+ and npm
- MongoDB instance (local or cloud)
- OpenAI API Key
- Git

## Setup & Installation
1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/chatbot-platform.git
   cd chatbot-platform
   ```

2. **Backend Setup**
   ```bash
   cd backend
   npm install
   ```

3. **Frontend Setup**
   ```bash
   cd ../frontend
   npm install
   ```

4. **Environment Variables**
   Create a `.env` file in both `backend` and `frontend` directories with the following keys:

   ```bash
   # Backend (.env)
   MONGODB_URI=your_mongodb_uri
   JWT_SECRET=your_jwt_secret
   OPENAI_API_KEY=your_openai_api_key
   PORT=5000

   # Frontend (.env)
   REACT_APP_API_URL=http://localhost:5000/api
   ```

5. **Start the Application**
   - **Backend**
     ```bash
     cd backend
     npm start
     ```
   - **Frontend**
     ```bash
     cd frontend
     npm start
     ```

The frontend will run on http://localhost:3000

---

## API Endpoints

### Authentication
- `POST /api/auth/register` — Register new user
- `POST /api/auth/login` — Log in

### Projects
- `GET /api/projects` — List user projects
- `POST /api/projects` — Create project
- `PUT /api/projects/:id` — Update project
- `DELETE /api/projects/:id` — Delete project

### Chat
- `POST /api/chat/:projectId` — Send message and receive AI response

---

## Deployment
This project is deployed on Railway. Changes to `main` branch auto-deploy to https://chatbot-platform-demo.railway.app

---

## Notes
- Ensure MongoDB connection is accessible from deployment environment.
- Use a valid OpenAI API key with sufficient quota.
- For file uploads, set up CORS and API permissions in OpenAI dashboard.
