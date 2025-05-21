<<<<<<< HEAD
# GUVI Hackathon FSD Setup

A full-stack development boilerplate for GUVI Hackathon participants, featuring a React frontend and Python backend.

## 🚀 Tech Stack

### Frontend
- React 18+ with Vite
- Tailwind CSS for styling
- Netlify for deployment

### Backend
- Python 3.x
- FastAPI
- Railway for deployment

## 📋 Prerequisites

### Common Requirements
- Git
- Make (GNU Make)
  - Windows: Install via [Chocolatey](https://chocolatey.org/install) or [Scoop](https://scoop.sh/)
  - macOS: Install via `xcode-select --install` or `brew install make`
  - Linux: Install via package manager (e.g., `sudo apt-get install make`)

### For Frontend Development
- Node.js (v22.13.1)
  - Windows: Download from [Node.js website](https://nodejs.org/)
  - macOS: Install via `brew install node@22` or use [nvm](https://github.com/nvm-sh/nvm)
  - Linux: Install via package manager or use [nvm](https://github.com/nvm-sh/nvm)
- npm or yarn package manager

### For Backend Development
- Python 3.x
  - Windows: Download from [Python website](https://www.python.org/downloads/)
  - macOS: Install via `brew install python@3.11` or download from Python website
  - Linux: Install via package manager (e.g., `sudo apt-get install python3.11`)
- pip (Python package manager)
- Virtual environment (recommended)

## 🛠️ Getting Started

### Important Note
This is a boilerplate template. Do not push directly to this repository. Instead:
1. Fork this repository to your GitHub account
2. Clone your forked repository
3. Create a new repository for your project
4. Push your code to your new repository

### Environment Variables

Both frontend and backend use environment variables for configuration. Create the following `.env` files:

#### Backend (.env)
Create `backend/.env`:
```env
APP_NAME=Hackathon FastAPI Backend
API_VERSION=v1
```

#### Frontend (.env)
Create `frontend/.env`:
```env
VITE_API_URL=http://localhost:3001
```

Note: `.env` files are not tracked in Git for security reasons. Make sure to:
1. Never commit `.env` files to version control
2. Keep a `.env.example` file in your repository as a template
3. Document all required environment variables in your README

### Clone Your Fork
```bash
git clone https://github.com/guvi-research/react-python-fsd-v1.git
cd react-python-fsd-v1
```

### Frontend Setup
1. Navigate to the frontend directory:
```bash
cd frontend
```

2. Using Make (Recommended):
```bash
make run-local
```
This command will:
- Check Node.js version
- Install dependencies
- Start the development server
- Open the browser automatically

If you encounter issues with `make run-local`, you can run the commands manually:
```bash
# 1. Install dependencies
npm install

# 2. Start the development server
npm run dev
```

The frontend will be available at `http://localhost:3000`

### Backend Setup
1. Navigate to the backend directory:
```bash
cd backend
```

2. Using Make (Recommended):
```bash
make run-local
```
This command will:
- Check Python installation
- Set up virtual environment
- Install dependencies
- Start the FastAPI server
- Open the API documentation in browser

If you encounter issues with `make run-local`, you can run the commands manually:
```bash
# 1. Create virtual environment
# Windows
python -m venv venv
.\venv\Scripts\activate

# macOS/Linux
python3 -m venv venv
source venv/bin/activate

# 2. Install dependencies
pip install -r requirements.txt

# 3. Start the server
uvicorn app.main:app --reload --port 3001
```

The backend will be available at `http://localhost:3001`
API documentation will be available at `http://localhost:3001/docs`

## 🚀 Deployment

### Frontend Deployment (Netlify)
Using Make (Recommended):
```bash
cd frontend
make deploy
```
This command will:
- Check Node.js version
- Install dependencies
- Build the project
- Guide you through Netlify deployment

If you encounter issues with `make deploy`, you can deploy manually:
```bash
# 1. Build the project
npm run build

# 2. Deploy to Netlify
npx netlify deploy --prod --dir=dist
```

### Backend Deployment (Railway)
Using Make (Recommended):
```bash
cd backend
make deploy
```
This command will:
- Check Railway CLI installation
- Verify authentication
- Guide you through Railway deployment

If you encounter issues with `make deploy`, you can deploy manually:
```bash
# 1. Install Railway CLI
npm install @railway/cli

# 2. Login to Railway
railway login

# 3. Initialize project
railway init

# 4. Deploy
railway up
```

## ⚠️ IMPORTANT: Production Environment Setup

> **CRITICAL STEP**: After deploying your backend to Railway, you MUST create a `.env.production` file in your frontend directory with the production backend URL before building and deploying the frontend.

1. Deploy your backend to Railway first
2. Get your backend URL from Railway (it will look like `https://your-app-name.railway.app`)
3. Create `frontend/.env.production`:
```env
VITE_API_URL=https://your-app-name.railway.app
```
4. Only then proceed with frontend deployment

If you skip this step, your frontend will not be able to connect to your backend in production!


## 📚 Learning Resources

### Frontend
- [React Documentation](https://react.dev)
- [Vite Documentation](https://vitejs.dev/guide/)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [Netlify Documentation](https://docs.netlify.com)

### Backend
- [FastAPI Documentation](https://fastapi.tiangolo.com/)
- [Python Documentation](https://docs.python.org/3/)
- [Railway Documentation](https://docs.railway.app)

## 🏗️ Project Structure

```
react-python-fsd-v1/
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   └── services/
│   ├── public/
│   ├── .env
│   ├── Makefile
│   └── package.json
└── backend/
    ├── app/
    │   ├── routes/
    │   ├── models/
    │   └── main.py
    ├── .env
    ├── Makefile
    └── requirements.txt
```

## 🔧 Available Make Commands

### Frontend
- `make run-local` - Start development server
- `make deploy` - Deploy to Netlify

### Backend
- `make run-local` - Start development server
- `make deploy` - Deploy to Railway

## 🤝 Contributing

1. Fork this repository to your GitHub account
2. Create a new repository for your project
3. Clone your forked repository
4. Make your changes
5. Push to your new repository

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.
=======
# 🧠 Resume Skill Extractor

**Resume Skill Extractor** is a full-stack AI-powered web application that automates the extraction of key skills from resumes. It simplifies and accelerates the screening process for recruiters and job platforms by instantly identifying and categorizing both technical and non-technical skills from uploaded documents.

> 🚀 Built for the **AKTU AI Tech Confluence Hackathon 2025**, organized by **GUVI** and **HCL**.

---

## 📌 Problem Statement

Build a solution that automates **skill extraction from resumes** using **Natural Language Processing (NLP)** to assist recruiters in efficient, unbiased, and rapid talent assessment.

---

## 👥 Team Doraemon

- 👤 **Priya Gupta [ME]**
- 👤 Uttam Kumar
- 👤 Sambhav Jain

---

## 🌟 Key Features

- 📄 Upload resumes in **PDF** or **text** format also drag and drop available to upload 
- 🧠 Automatically extract **technical and non-technical skills**  
- 🔎 Leverages **NLP** to parse and analyze resume text  
- 💡 Clean, categorized skill output in real-time  
- 🌐 User-friendly web interface with **React** frontend  
- ⚙️ Robust **Python FlaskAPI** backend

---

## 🛠️ Tech Stack

### 🎯 Frontend  
- **React.js**  
- Deployed on **Netlify**

### ⚙️ Backend  
- **Python FlaskAPI**  
- Deployed on **Railway**

### 🧠 Core Logic  
- **Natural Language Processing (NLP)**

---

## 🚀 How It Works

1. 👤 User uploads their resume via the web interface  
2. 🧠 Flask API processes and parses the content using NLP  
3. 🧾 Extracted skills are categorized and returned as structured data  
4. 🌐 Frontend displays the results in a neat and interactive format

---

## 📈 Impact

- ⏱️ Significantly reduces manual screening time  
- 📋 Enhances accuracy and consistency in skill evaluation  
- 🎯 Supports recruiters in making faster, smarter hiring decisions

---

## 🤝 Acknowledgment

This project was developed as part of the **AKTU AI Tech Confluence Hackathon 2025**, proudly hosted by **GUVI** and **HCL**.
>>>>>>> origin/main
