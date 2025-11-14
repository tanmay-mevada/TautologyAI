# TautologyAI - Legal Document Analysis Platform

**Tech Stack:** Next.js 15.5.2 | FastAPI | Firebase Hosting | Google Cloud AI | Supabase

> AI-powered platform that analyzes legal documents to deliver instant summaries, risk detection, and plain-language explanations without requiring legal expertise.

## Project Overview

TautologyAI is an AI-powered platform designed to demystify legal documents for everyone. Built for the Gen AI Exchange Hackathon, our solution makes advanced legal document analysis accessible to legal professionals, businesses, and individuals without requiring extensive legal training or expensive consultation fees.

### Problem Statement
Student Track: Generative AI for Demystifying Legal Documents

### Team TurboC++
- Tanmay Mevada - tanmaymevada24@gmail.com  
- Jaiveek Chauhan - jaivikchauhan2007@gmail.com
- Manash Gusani - manashgusani427@gmail.com
- Rajveer Jadeja - rajveersinhjadeja@gmail.com
- Nishith Bodar - bodarnishith32@gmail.com

## Key Features

### Smart Document Processing
- Advanced OCR and AI analysis for PDFs, contracts, and legal documents
- High accuracy text extraction and content understanding
- Multi-format document support

### Instant Analysis
- Comprehensive summaries in seconds
- Risk assessments and red flag identification
- Key party identification and clause extraction

### Risk Detection
- Automatic identification of potential risks
- Important clause highlighting
- Negotiation point suggestions

### Interactive Q&A
- Ask questions about your documents
- Get clear, contextual answers
- AI-backed analysis and explanations

### Modern Web Interface
- Responsive design for all devices
- Dark/light mode support
- Intuitive user experience
- Real-time processing updates

## Architecture

```
TautologyAI/
├── Frontend (Next.js 15.5.2)
│   ├── Static site generation
│   ├── Firebase Hosting
│   ├── Tailwind CSS styling
│   └── React components
└── Backend (FastAPI + Python)
    ├── Google Cloud Document AI
    ├── Vertex AI & Gemini
    ├── Firebase Admin SDK
    └── Supabase Database
```

## Tech Stack

### Frontend
- **Framework:** Next.js 15.5.2 with React 19
- **Styling:** Tailwind CSS + Shadcn/UI components
- **Authentication:** Firebase Auth (Google OAuth)
- **Deployment:** Firebase Hosting (Static Export)
- **Icons:** Lucide React
- **Email:** Nodemailer for contact forms

### Backend
- **API:** FastAPI with Python 3.11+
- **AI Processing:** Google Cloud Document AI + Vertex AI
- **Database:** Supabase (PostgreSQL)
- **Storage:** Firebase Storage
- **Deployment:** Google Cloud Run
- **Authentication:** Firebase Admin SDK

### AI & Cloud Services
- **OCR:** Google Cloud Document AI
- **LLM:** Gemini 2.5 Flash Lite
- **Cloud Platform:** Google Cloud Platform
- **Authentication:** Firebase Auth
- **Database:** Supabase
- **Storage:** Firebase Storage

## Quick Start

### Prerequisites
- Node.js 18+ and npm
- Python 3.11+
- Firebase account
- Google Cloud account
- Supabase account

### Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

**Environment Variables (.env.local):**
```env
NEXT_PUBLIC_FIREBASE_API_KEY=your_firebase_api_key
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=your_project.firebaseapp.com
NEXT_PUBLIC_FIREBASE_PROJECT_ID=your_project_id
NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=your_project.appspot.com
NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
NEXT_PUBLIC_FIREBASE_APP_ID=your_app_id

# Email Configuration
EMAIL_USER=your-email@gmail.com
EMAIL_PASS=your-app-specific-password
```

### Backend Setup

```bash
cd backend
pip install -r requirements.txt
uvicorn main:app --reload
```

**Environment Variables (.env):**
```env
SUPABASE_URL=your_supabase_url
SUPABASE_SERVICE_ROLE_KEY=your_service_role_key
GCP_PROJECT_ID=your_gcp_project
DOC_AI_PROCESSOR_ID=your_processor_id
GEMINI_MODEL=gemini-2.5-flash-lite
FIREBASE_PROJECT_ID=your_firebase_project
ADMIN_EMAILS=admin1@email.com,admin2@email.com
```

## Project Structure

```
legal-ai/
├── README.md                    # Documentation
├── LICENSE                      # MIT License
├── database_setup.sql          # Database schema
├── 
├── frontend/                    # Next.js Frontend
│   ├── src/
│   │   ├── app/                 # App Router pages
│   │   │   ├── page.tsx           # Main dashboard
│   │   │   ├── about/             # About & contact page
│   │   │   ├── upcoming-features/ # Roadmap page
│   │   │   └── api/contact/       # Contact API route
│   │   ├── components/ui/      # Reusable UI components
│   │   └── lib/                # Utilities & config
│   ├── public/                 # Static assets
│   ├── firebase.json          # Firebase hosting config
│   ├── next.config.ts         # Next.js config
│   └── package.json           # Dependencies
│   
└── backend/                     # FastAPI Backend
    ├── app/
    │   ├── api/                   # API routes
    │   └── core/                  # Core utilities
    ├── Dockerfile             # Container config
    ├── requirements.txt       # Python dependencies
    └── main.py                # FastAPI app entry
```

## Key Pages & Features

### Main Dashboard
- Google OAuth authentication
- File upload interface
- Document processing status
- Results display and interaction

### About & Contact
- Hackathon project information
- Team member details
- Project resources and links
- Contact form with email integration
- Social media links

### Upcoming Features
- Development roadmap
- Feature timeline and priorities
- User feedback collection
- GitHub integration links

## Deployment

### Frontend (Firebase Hosting)
```bash
npm run build
npm run deploy
```

### Backend (Google Cloud Run)
```bash
./deploy.sh  # Automated deployment script
```

## API Endpoints

### Authentication
- `GET /` - Health check
- Protected routes require Firebase JWT token

### Document Processing
- `POST /api/upload` - Upload and process documents
- `GET /api/documents` - List user documents
- `POST /api/analyze` - Analyze document content

### Contact
- `POST /api/contact` - Send contact form emails

## UI Components

Built with Shadcn/UI and Tailwind CSS:
- Button - Interactive buttons with variants
- Card - Content containers
- Input & Textarea - Form inputs
- Badge - Status indicators
- ScrollArea - Scrollable content areas

## Performance & SEO

- Static Site Generation for optimal performance
- Responsive design for all devices
- SEO optimized with proper meta tags
- Firebase CDN for global content delivery

## Security Features

- Firebase Authentication with Google OAuth
- JWT token validation on all protected routes
- Admin role management via environment variables
- Secure file uploads to Firebase Storage
- Environment variable protection for sensitive data

## Contact & Support

- **Email:** turbo.cpp.nu@gmail.com
- **GitHub:** [tanmay-mevada/legal-ai](https://github.com/tanmay-mevada/legal-ai)
- **Instagram:** [@turbo.cpp.nu](https://www.instagram.com/turbo.cpp.nu)

## Resources

- **Presentation:** [View Slides](https://storage.googleapis.com/vision-hack2skill-production/innovator/USER00972666/1758477302364-GenAIExchangeHackathonPrototypeSubmissionByTautologyAITurboC.pdf)
- **Demo Video:** [Watch Demo](https://youtu.be/8r8_jnx0UBs?si=1yOqEsTlGbypWcb_)
- **Source Code:** [GitHub Repository](https://github.com/tanmay-mevada/Legal-AI)

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Hackathon Context

This is a prototype application developed for the Gen AI Exchange Hackathon. The project demonstrates the potential of AI in democratizing legal document analysis and making legal technology more accessible to everyone.

---

© 2025 TautologyAI - Team TurboC++
