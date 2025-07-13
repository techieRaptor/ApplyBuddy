
# 🚀 ApplyBuddy

**Your AI-powered Job Search Sidekick**

## ✨ Overview

**ApplyBuddy** automates boring job searches and applications so you can focus on cracking interviews!  
It finds relevant jobs, generates customized cover letters with AI, and even applies for you — while you track everything in a simple dashboard.

✅ Automates job searching with web scraping  
✅ Generates tailored cover letters using AI  
✅ Fills application forms automatically (where possible)  
✅ Tracks your applications, status, and approvals

---

## 🛠️ Tech Stack

| Layer | Tech |
|-------|------|
| **Backend** | Spring Boot (Java) |
| **Scraper** | Python + Selenium |
| **AI Service** | Python + Local LLM (Ollama) or OpenAI API |
| **Frontend** | ReactJS |
| **Database** | PostgreSQL (or SQLite for local) |
| **DevOps** | Docker & Docker Compose |

## 🔗 Architecture Blueprint

ApplyBuddy is designed with a modular microservice pattern so each part is independent and easy to test.
[ React Dashboard ]
       |
   [ Spring Boot API ]
       |
   ┌─────────────┐ ┌─────────────┐
   │ Python Scraper │ │ Python AI Service │
   └─────────────┘ └─────────────┘
       |
   [ PostgreSQL DB ]

## ⚙️ How It Works

✅ **Scraper Module**  
- Logs in to job sites like Naukri using Selenium.
- Searches for jobs based on your preferences.
- Saves job data to the DB.

✅ **AI Service**  
- Takes your base CV + job description.
- Uses local LLM or GPT API to generate a unique cover letter.
- Stores the output in the DB.

✅ **Backend API (Spring Boot)**  
- Handles user auth, job data, status updates.
- Exposes REST endpoints for the frontend.

✅ **Frontend (React)**  
- Shows new jobs found by the scraper.
- Displays the AI-generated cover letters.
- Lets you approve or auto-apply.
- Tracks status in one dashboard.

## 📂 Project Structure

/ApplyBuddy
 ├── backend-springboot/      # Spring Boot REST API
 ├── scraper-service/         # Python Selenium job scraper
 ├── ai-service/              # Python AI microservice
 ├── frontend-react/          # ReactJS dashboard
 ├── db/                      # DB schema and init scripts
 ├── docs/                    # Diagrams & blueprint docs
 ├── docker-compose.yml       # Orchestration for local dev
 ├── .gitignore               # Ignore secrets & build junk
 └── README.md                # You’re reading it!

## ⚡ Getting Started

1️⃣ **Clone the Repo**

git clone https://github.com/techieRaptor/ApplyBuddy.git

2️⃣ **Set up your `.env` files**

# backend-springboot/.env
DB_URL=
DB_USER=
DB_PASSWORD=

# ai-service/.env
OPENAI_API_KEY=

3️⃣ **Run with Docker Compose**

docker-compose up --build

OR run each module manually for dev.

## ✅ Status

| Module | Status |
|--------|--------|
| Scraper | 🟢 Basic job search working |
| AI Service | 🟢 Generates simple cover letters |
| Backend API | 🟢 Exposes job + apply endpoints |
| Frontend | 🟢 Basic dashboard shows job list |
| DB | 🟢 Local Postgres with schema |

## 📸 Screenshots & Docs

👉 See `/docs/architecture-diagram.png` for full blueprint  
👉 See `/docs/sequence-diagram.png` for data flow  
👉 Add screenshots or GIFs here once your React dashboard is ready!

## 🚩 Disclaimer

> **ApplyBuddy** is a personal, educational project.  
> Always respect each job portal’s Terms of Service — scraping may not be allowed for commercial use.  
> Keep your login credentials and API keys secret — never commit them to GitHub!

## 🤝 Author

Built with ❤️ by **Satish Kumar**

**LinkedIn:** [Your LinkedIn URL]  
**Portfolio:** [Your website if you have one]

## 📢 License

Open-source for personal, non-commercial use.  
Feel free to fork and adapt — credits appreciated! 🎉
