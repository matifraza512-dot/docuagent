 🚀 DocuAgent - AI-Powered Documentation Assistant

Python 3.11+ FastAPI React TypeScript MIT License Discord

🤖 AI That Writes Documentation So You Don't Have To

DocuAgent is an open-source AI assistant that automatically generates, maintains, and explains technical documentation. It turns your codebase into comprehensive, always-accurate documentation using RAG (Retrieval-Augmented Generation) and autonomous AI agents.

"The missing piece between your code and understandable documentation"

✨ Features

Feature                     Description                                       Status
🤖 Code-to-Docs AI          Automatically generates documentation from source code   🟢 MVP
🔍 Smart Code Analysis      Understands context, patterns, and dependencies         🟢 MVP
💬 Documentation Chatbot    Ask questions about your codebase in plain English      🟡 In Progress
🔄 Version-Aware Docs       Links documentation to specific git commits             🟡 In Progress
🔧 Multi-Language Support   Python, JavaScript, TypeScript, Go, Java              🟢 MVP
🚀 Self-Hosted              Run locally or in your private cloud                   🟢 Ready
📊 API Documentation        Auto-generates OpenAPI/Swagger specs                   🟡 In Progress

🏗️ Architecture

Code Repository → Code Analyzer → Vector Database (pgvector)
               ↘ Git History Parser ↗

User Query → AI Agent Orchestrator → RAG Pipeline (LangChain + LlamaIndex) → LLM Response Generator (Ollama/OpenAI) → Formatted Documentation (Markdown/HTML/PDF) → Interactive UI (React + FastAPI)

🚀 Quick Start

Option 1: Docker (Recommended)

git clone https://github.com/matifraza512-dot/docuagent.git
cd docuagent
docker-compose up -d
open http://localhost:3000  # Frontend
open http://localhost:8000/docs  # API Documentation

Option 2: Local Development

Backend Setup:
cd backend
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
uvicorn app.main:app --reload

Frontend Setup (in another terminal):
cd frontend
npm install
npm run dev

📚 Use Cases

👤 Individual Developers

Example: Before vs After DocuAgent

Before: Undocumented function
def process_data(input):
    # ... complex logic ...
    return result

After DocuAgent:
def process_data(input: Dict[str, Any]) -> pd.DataFrame:
    """
    Processes input data through transformation pipeline.
    
    Args:
        input: Dictionary containing raw data with keys:
            - 'users': List of user dictionaries
            - 'config': Processing configuration
            
    Returns:
        Cleaned and normalized pandas DataFrame
        
    Raises:
        ValueError: If input format is invalid
        ProcessingError: If transformation fails
    """

👥 Engineering Teams
• Onboarding: New hires understand codebase in days, not weeks
• Knowledge Transfer: Preserve institutional knowledge
• Code Reviews: Automated documentation checks in PRs
• Technical Debt: Identify undocumented or complex code

🌍 Open Source Maintainers
• Keep documentation synchronized with rapid development
• Community contributions become easier to review
• Automated changelog generation from commits

🛠️ Tech Stack

Layer           Technology                    Purpose
Frontend        React 18 + TypeScript + Vite  Modern, fast UI development
UI Components   shadcn/ui + Tailwind CSS      Beautiful, accessible components
Backend         FastAPI + Python 3.11         High-performance async API
AI/ML           Ollama, LangChain, LlamaIndex Local LLMs, RAG pipelines
Database        PostgreSQL + pgvector         Relational + vector search
Search          Qdrant (optional)             High-performance vector search
Container       Docker + Docker Compose       Consistent environments
CI/CD           GitHub Actions                Automated testing & deployment

🎯 Roadmap

Phase 1: Core Documentation (Now)
✓ Basic repository setup
• Code analysis for Python/JavaScript
• Simple documentation generation
• Basic web interface

Phase 2: Advanced AI (Q1 2024)
• RAG-powered Q&A system
• Multi-repository analysis
• VS Code extension
• Git integration

Phase 3: Enterprise Features (Q2 2024)
• Team collaboration features
• SSO integration
• Advanced analytics
• API marketplace

Phase 4: Ecosystem (Q3 2024)
• Plugin system
• CI/CD integrations
• Mobile app
• Desktop application

🤝 Contributing

We love contributions! See our detailed Contributing Guide.

First time contributing? Check out our Good First Issues.

Development Setup:

1. Fork the repository
2. Clone your fork: git clone https://github.com/YOUR_USERNAME/docuagent.git
3. Create a feature branch: git checkout -b feature/amazing-feature
4. Make your changes and test
5. Commit with semantic messages: git commit -m "feat: add code analysis for TypeScript"
6. Push to your fork: git push origin feature/amazing-feature
7. Open a Pull Request

📊 Project Statistics

GitHub Stars: (badge will appear)
GitHub Forks: (badge will appear)
GitHub Issues: (badge will appear)
GitHub PRs: (badge will appear)

🏆 Acknowledgments

• LangChain for the amazing AI orchestration framework
• Ollama for making local LLMs accessible
• FastAPI for the incredible Python web framework
• The open source community for inspiration and support

📄 License

MIT License - see LICENSE file for details.

Copyright (c) 2024 Atif Raza - GitHub | LinkedIn

---

⭐ Star this repo if you find it useful!
🐛 Found a bug? Open an Issue
💡 Have an idea? Start a Discussion

"Good code explains what, great documentation explains why."
