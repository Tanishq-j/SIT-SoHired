# 🎓 SoHired | Career Guidance & Skill Gap Analyzer

*SoHired* is an AI-driven platform built to eradicate the "employability gap." We analyze a student's academic performance, personal interests, and current skills to intelligently suggest tailored career paths. By comparing their profile against real-time industry requirements, we don't just point out what they are missing—we provide the exact free/paid courses and micro-lessons they need to become job-ready.

---

# ✨ Key Highlights & Features

* 🎯 *Dynamic Career Path Mapping:* Whether a student is a clueless first-year (using text input to gauge interests) or a graduating senior (uploading a resume), our Gemini engine maps their profile to the perfect tech role (e.g., Frontend, Cloud, Data).
* 🔍 *Profile vs. Industry Gap Analysis:* The AI performs a deep-context comparison between the student's current skill set and live job market requirements, pinpointing exact technical deficits.
* ⏱️ *The "Micro-Cheat" Learning Engine:* Professionals and students don't have time for fluff. When a skill gap is found, our system dynamically hunts down the best YouTube tutorial, parses the transcript, and extracts the exact start and end timestamps to deliver a hyper-focused 3-minute lesson.
* 📚 *Actionable Upskilling Roadmaps:* Curates a personalized dashboard of free and paid courses (e.g., Coursera, Udemy) specifically targeted to bridge the identified gaps.

---

# 🏗️ System Architecture & AI Workflow

graph TD
    A[Student Onboarding] -->|Newbie: Interests & Hobbies| B(Generate Holistic Profile)
    A -->|Senior: Academic Record & Resume| B
    
    B --> C{Google Gemini: Career Path Mapping}
    C --> D[Suggest Target Industry Role]
    
    D --> E{Google Gemini: Skill Gap Analyzer}
    E -->|Profile vs. Industry Needs| F[Identify Exact Missing Skills]
    
    F --> G[Generate Upskilling Roadmap]
    G --> H[Recommend Free/Paid Courses]
    G --> I[YouTube API + Transcript Parsing]
    
    I --> J{Google Gemini: Timestamp Extraction}
    J --> K[Deliver Exact Micro-Lesson]

🧠 Google Gemini Integration
We heavily utilize Google Gemini Pro to power the core logic of the platform:

Interest-to-Role Translation: Turning vague student inputs ("I like making things look good") into concrete career paths ("UI/UX Designer").

Contextual Gap Detection: Moving beyond simple keyword matching to understand the semantic difference between a student's academic projects and industry-grade requirements.

Timestamp Extraction: Feeding raw JSON arrays of YouTube subtitles into the LLM to identify contextual topic changes and return exact integer offsets for our video player.

💻 Tech Stack
Frontend:

React.js (Dynamic Dashboards & Roadmaps)
Tailwind CSS (Modern, accessible UI)

Backend & AI:

Node.js & Express.js (API routing & Pipeline orchestration)
Firebase (Student profiles, course databases)
Google Gemini Pro (Core AI Intelligence Engine)

Micro-Learning Integrations:

yt-search: Programmatic tutorial discovery.
youtube-transcript: Extracting captions for AI timestamp analysis.
   
🚀 Getting Started (Local Development)
1. Clone the repository
Bash
git clone https://github.com/yourusername/sohired.git
cd sohired
2. Install Dependencies
Bash
# Install backend dependencies
cd backend
npm install

# Install frontend dependencies
cd ../frontend
npm install
3. Environment Variables
Create a .env file in the backend directory:

Code snippet
PORT=5000
MONGO_URI=your_mongodb_connection_string
GEMINI_API_KEY=your_google_gemini_api_key
4. Run the Application
Bash
# Start backend
npm run dev

# Start frontend
npm start
Built to bridge the gap between graduation and employment.
