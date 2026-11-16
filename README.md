UniversityHub - The Campus Operating System

UniversityHub is an open-source, clean, and structured platform designed to replace the chaotic environment of university WhatsApp groups. It serves as a single "Campus Operating System" for students, professors, and societies.

The Problem:
Currently, students miss important campus updates, past papers are lost in WhatsApp chats, and there is no centralized way for societies to announce events.

The Solution (Core Features):
*   Daily Campus Feed: A personalized feed showing what's happening on campus today.
*   Pinned Resources Library: A searchable database for past papers and notes.
*   Professor & Course Pages: Official spaces for announcements.
*   Society Hubs: Dedicated profiles for university societies.
*   Anonymous Q&A: A safe space to ask questions without revealing identity.

 UI/UX Vision (The Interface):
*   Theme: Clean, Light, and Minimalist. 
*   Color Palette:Soft Lime Green (Primary), White (Background), and Dark Gray (Text).
*   Inspiration: Notion's cleanliness with Reddit's community feel. No dark mode as default.

 Tech Stack:

 Frontend:
*   HTML/CSS/JavaScript: The core basics (No complex frameworks to start).
*   Tailwind CSS: For fast, beautiful, and light lime styling (Very easy to learn).
*   Fetch API: Built-in JavaScript feature to talk to the backend (No Axios needed).

 Backend:
*   Python (FastAPI): High-performance backend framework (You already know this!).
*   SQLAlchemy: To talk to the database.
*   JWT: For secure Login/Signup.

 Database & Caching:
*   PostgreSQL: Primary database.
*   Redis: For caching (Making the feed fast).

 DevOps & Tools:
*   Docker & Docker Compose: To run everything together.
*   Git & GitHub: For version control.

 Database Schema:
1.  Users: `id`, `name`, `email`, `password`, `role` (Student/Professor).
2.  Posts: `id`, `user_id`, `content`, `created_at`.
3.  Resources: `id`, `subject`, `semester`, `file_url`, `uploaded_by`.
4.  Societies: `id`, `name`, `description`.

 Folder Structure:

UniversityHub/
│
├── backend/                  # FastAPI Backend
│   ├── app/
│   │   ├── routes/           # API endpoints (users, posts)
│   │   ├── models/           # Database tables
│   │   ├── database.py       # DB Connection
│   │   └── main.py           # Entry point
│   ├── requirements.txt
│   └── Dockerfile
│
├── frontend/                 # Simple Frontend
│   ├── index.html            # Main page
│   ├── style.css             # Tailwind CSS
│   └── app.js                # Fetch API logic
│
├── docker-compose.yml        # Docker setup
└── README.md

 How to Run (Local Setup):
**Clone the repository:

bash
git clone https://github.com/YOUR_USERNAME/UniversityHub.git
cd UniversityHub

**Run with Docker:

bash
docker-compose up --build
