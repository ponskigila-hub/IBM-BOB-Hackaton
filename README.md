# RepoLens AI 🔍

> Understand Any Repository Instantly

AI-powered GitHub repository analyzer that provides instant insights about any codebase. Built for the IBM Bob Hackathon.

![RepoLens AI](https://img.shields.io/badge/Status-MVP-green)
![License](https://img.shields.io/badge/License-MIT-blue)

## 🎯 Problem Statement

Developers spend **hours** understanding new codebases:
- Reading through hundreds of files
- Deciphering architecture patterns
- Finding critical components
- Understanding project structure

**RepoLens AI reduces this from hours to minutes.**

## 💡 Solution

Paste any GitHub repository URL and get:
- **Project Summary**: What it does and why it exists
- **Architecture Analysis**: Structure, patterns, and components
- **Important Files**: Critical files and their purposes
- **Improvement Suggestions**: Actionable recommendations
- **Onboarding Guide**: How to get started quickly

## ✨ Features

- 🚀 **Instant Analysis**: Results in seconds
- 🤖 **AI-Powered**: Uses IBM Bob for intelligent insights
- 🎨 **Modern UI**: Clean, responsive interface
- 📊 **Comprehensive**: Multiple analysis dimensions
- 🔒 **No Auth Required**: Simple and fast

## 🏗️ Architecture

```
┌─────────────┐      ┌──────────────┐      ┌─────────────┐
│   Frontend  │─────▶│   Backend    │─────▶│  IBM Bob AI │
│  (Next.js)  │      │  (FastAPI)   │      │             │
└─────────────┘      └──────────────┘      └─────────────┘
                            │
                            ▼
                     ┌──────────────┐
                     │   GitHub     │
                     │ (Clone Repo) │
                     └──────────────┘
```

## 🛠️ Tech Stack

### Frontend
- **Framework**: Next.js 14
- **Language**: TypeScript
- **Styling**: Tailwind CSS
- **Deployment**: Vercel

### Backend
- **Framework**: FastAPI
- **Language**: Python 3.11+
- **AI**: IBM Bob API
- **Deployment**: Render

## 📦 Installation

### Prerequisites
- Node.js 18+
- Python 3.11+
- Git
- IBM Bob API Key

### Backend Setup

```bash
cd backend

# Install dependencies
pip install -r requirements.txt

# Configure environment
cp .env.example .env
# Edit .env and add your IBM_BOB_API_KEY

# Run server
python main.py
```

Backend runs on `http://localhost:8000`

### Frontend Setup

```bash
cd frontend

# Install dependencies
npm install

# Configure environment
cp .env.example .env.local
# Edit .env.local if needed

# Run development server
npm run dev
```

Frontend runs on `http://localhost:3000`

## 🚀 Usage

1. **Open the app** at `http://localhost:3000`
2. **Paste a GitHub URL** (e.g., `https://github.com/vercel/next.js`)
3. **Click "Analyze Repository"**
4. **View comprehensive analysis** in seconds

### Example Repositories to Try

- `https://github.com/vercel/next.js`
- `https://github.com/facebook/react`
- `https://github.com/microsoft/vscode`

## 📁 Project Structure

```
RepoLens-AI/
├── backend/                 # FastAPI backend
│   ├── main.py             # Application entry point
│   ├── routes/             # API endpoints
│   ├── services/           # Business logic
│   │   ├── repo_cloner.py  # GitHub cloning
│   │   ├── file_scanner.py # File analysis
│   │   ├── prompt_builder.py # AI prompts
│   │   └── analysis_service.py # IBM Bob integration
│   └── utils/              # Utilities
│
├── frontend/               # Next.js frontend
│   ├── app/               # Pages and layouts
│   ├── components/        # React components
│   ├── services/          # API integration
│   └── types/             # TypeScript types
│
└── README.md              # This file
```

## 🔌 API Endpoints

### POST `/api/analyze`

Analyze a GitHub repository.

**Request:**
```json
{
  "github_url": "https://github.com/user/repo",
  "use_mock": false
}
```

**Response:**
```json
{
  "success": true,
  "summary": "Project description...",
  "architecture": "Architecture explanation...",
  "important_files": [...],
  "suggestions": [...],
  "onboarding": "Getting started guide...",
  "repo_info": {
    "name": "user_repo",
    "technologies": ["Python", "JavaScript"],
    "file_count": 42,
    "total_lines": 1500
  }
}
```

## 🎨 Screenshots

### Landing Page
Clean, modern interface with GitHub URL input.

### Analysis Results
Comprehensive breakdown of repository structure and insights.

### Loading State
Animated loading indicator during analysis.

## 🚢 Deployment

### Backend (Render)

1. Create new Web Service
2. Connect GitHub repository
3. Set build command: `pip install -r requirements.txt`
4. Set start command: `uvicorn main:app --host 0.0.0.0 --port $PORT`
5. Add environment variable: `IBM_BOB_API_KEY`
6. Deploy

### Frontend (Vercel)

1. Import GitHub repository
2. Framework preset: Next.js
3. Add environment variable: `NEXT_PUBLIC_API_URL`
4. Deploy

## 🧪 Testing

### Backend

```bash
cd backend

# Test with mock data
curl -X POST http://localhost:8000/api/analyze \
  -H "Content-Type: application/json" \
  -d '{"github_url": "https://github.com/user/repo", "use_mock": true}'
```

### Frontend

```bash
cd frontend
npm run dev
# Open http://localhost:3000 and test manually
```

## 🎯 Hackathon Criteria

### Innovation
- Novel approach to code understanding
- AI-powered analysis reduces manual effort
- Instant insights vs. hours of reading

### Technical Excellence
- Clean, modular architecture
- Type-safe TypeScript frontend
- Robust error handling
- Production-ready code

### User Experience
- Simple, intuitive interface
- Fast response times
- Clear, actionable insights
- Responsive design

### Impact
- **Reduces onboarding time** from hours to minutes
- **Improves code review** efficiency
- **Accelerates development** workflow
- **Helps developers** understand legacy code

## 🔮 Future Improvements

- 🔐 **Authentication**: User accounts and history
- 💾 **Database**: Save analysis results
- 📊 **Visualizations**: Dependency graphs and charts
- 🔍 **Deep Analysis**: Security scanning, performance metrics
- 🤝 **Collaboration**: Team sharing and comments
- 🔌 **Integrations**: VSCode extension, GitHub App
- 📝 **Documentation**: Auto-generate docs from code
- 🧪 **Testing**: Suggest test cases and coverage

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

MIT License - see LICENSE file for details

## 👥 Team

Built with ❤️ for the IBM Bob Hackathon

## 🙏 Acknowledgments

- **IBM Bob** for AI capabilities
- **Next.js** for the amazing framework
- **FastAPI** for the fast backend
- **Tailwind CSS** for beautiful styling

## 📞 Contact

For questions or feedback, please open an issue on GitHub.

---

**RepoLens AI** - Understand Any Repository Instantly 🚀