# 🧠 MindAura – AI Burnout & Wellness Assistant  
**Developed by Shashank Dadhich**  
An AI-powered system designed to detect early signs of burnout, predict risk levels, and promote employee well-being through personalized insights, analytics, and an AI wellness coach.

---

## 🎬 Live Demo  
▶️ [Watch the Demo Video on YouTube](https://youtu.be/PcRpeq2zn9E)

---

## 🌟 Overview  
**MindAura** combines Artificial Intelligence, Natural Language Processing, and Behavioral Analytics to continuously monitor workplace well-being.  
It predicts burnout risk, identifies key stress factors, and provides personalized recommendations using Explainable AI and an interactive, gamified dashboard.

## 📸 Interface Previews  

<p align="center">
  <img src="assets/screenshots/dashboard.png" alt="Dashboard" width="65%" style="border-radius:10px; box-shadow:0 0 10px rgba(0,0,0,0.1);" />
</p>

<p align="center">
  <img src="assets/screenshots/insights.png" alt="Insights" width="65%" style="border-radius:10px; box-shadow:0 0 10px rgba(0,0,0,0.1);" />
</p>

<p align="center">
  <img src="assets/screenshots/stress_factors.png" alt="Stress Factors" width="65%" style="border-radius:10px; box-shadow:0 0 10px rgba(0,0,0,0.1);" />
</p>

<p align="center">
  <img src="assets/screenshots/ai_coach.png" alt="AI Coach" width="65%" style="border-radius:10px; box-shadow:0 0 10px rgba(0,0,0,0.1);" />
</p>


---

## 🚀 Key Features  

### 🔹 **1. Burnout Risk Dashboard**
- Displays real-time **Burnout Score** (0–100%) with mood colors:
  - 0–25% → Neutral (Teal)  
  - 25–50% → Calm (Blue)  
  - 50–75% → Concerned (Amber)  
  - 75–100% → Burnout (Red–Purple)
- Interactive burnout meter with pulse animation and historical trend graph.

---

### 🔹 **2. Real-Time Wellness Monitoring**
- Tracks emotional tone, meeting frequency, typing speed, and message sentiment.  
- Detects behavioral patterns leading to stress or fatigue.  
- Generates automatic daily and weekly wellness reports.

---

### 🔹 **3. Top Stress Contributors**
**Dashboard Section:**

| Contributor | Impact |
|--------------|--------|
| 🗓️ Meeting Overload | 42% |
| 💬 Negative Sentiment | 31% |
| 🌙 Low Sleep Hours | 27% |

---

### 🔹 **4. Explainable AI Insights (XAI)**
**Why This Score?**

| Factor | Impact on Burnout |
|---------|-------------------|
| Meeting Load | +22% |
| Negative Sentiment | +15% |
| Reduced Breaks | +12% |
| Sleep Quality | +18% |
| Work Hours | +10% |

**What-If Simulator:**  
Predictive module lets users adjust parameters:  
```
Meeting Hours: 6h/day  
Sleep Hours: 6h/night  
Predicted Burnout: 81%
```
💡 Adjust sliders → watch predicted burnout score change live.

---

### 🔹 **5. AI Mood Coach**
- Conversational and empathetic chatbot powered by NLP.  
- Gives mental wellness guidance and micro-interventions (“Take a 10-min walk”, “Reflect on your day”).  
- Emotionally aware — tone and avatar glow change with user state.

---

### 🔹 **6. Burnout Calculator & Risk Predictor**
- Backend ML model processes multiple features:
  - Work hours, sleep, sentiment, calendar events, rest breaks.  
- Outputs risk score and confidence level.  
- Predicts burnout trend over time.

---

### 🔹 **7. Behavior & Email Analysis**
- Uses sentiment analysis (BERT/NLP) to track communication tone.  
- Aggregates meeting frequency, response delay, and emotional polarity.  
- Generates visual reports for HR or personal use.

---

### 🔹 **8. Journals & Previous Entries**
- Text/voice mood journaling system.  
- AI summarizes weekly emotional trends.  
- Helps users reflect on personal well-being progress.

---

### 🔹 **9. Personalized Chatbot & Wellness Challenges**
- “MindAura Coach” interacts dynamically with each user.  
- Issues small daily challenges (hydration, reflection, stretch).  
- Tracks user engagement with a reward system.

---

### 🔹 **10. Gamification & Achievements**
- Badges like “Calm Champion”, “Focus Pro”, and “Resilience Rising.”  
- Streak tracker for consistent wellness actions.  
- Leaderboard (optional) for team-based engagement.

---

### 🔹 **11. Reports & Analytics**
- **Email Reports:** Auto-generated weekly summaries sent via backend scheduler.  
- **Graphical Analytics:** Line charts, heatmaps, radar graphs for stress, sleep, and emotion patterns.  
- **Departmental Insights:** Aggregate burnout heatmaps for HR teams (anonymous).

---

## 🧩 Project Architecture  

```plaintext
MindAura/
├── frontend/                  # React.js Interface
│   ├── components/            # Dashboard, Mood Coach, Graphs
│   ├── pages/                 # Home, Analytics, Profile, Journal
│   ├── assets/                # Icons, Animations, Lottie Files
│   ├── services/              # API Integration Layer
│   └── App.jsx
│
├── backend/                   # FastAPI Backend
│   ├── main.py                # API Endpoints
│   ├── model.pkl              # ML Burnout Prediction Model
│   ├── sentiment_analyzer.py  # NLP Sentiment Module
│   ├── burnout_predictor.py   # ML-based Risk Calculator
│   ├── scheduler.py           # Email & Report Automation
│   └── database.py            # SQLite/MongoDB Setup
│
├── data/                      # Training Data (optional)
├── README.md
├── LICENSE
├── .gitignore
└── package.json
```

---

## 📊 Flow Diagram

**Data Flow:**
```
User Activity → Data Processing → ML Burnout Model → API → React Dashboard → Visualization + AI Coach
```

**Pipeline Breakdown:**
1. **Data Ingestion:** Collects activity, sentiment, sleep, and communication logs.  
2. **Preprocessing:** Cleans and normalizes input data.  
3. **ML Model:** Predicts burnout risk using regression/classification.  
4. **FastAPI Backend:** Exposes REST APIs to the frontend.  
5. **React Dashboard:** Visualizes burnout trends and analytics.  
6. **AI Mood Coach:** Engages user with personalized guidance.  

---

## 🧠 Technologies Used

| Category | Tools |
|-----------|-------|
| Frontend | React.js, Tailwind CSS, Chart.js, Lottie Animations |
| Backend | Python, FastAPI, Uvicorn |
| Machine Learning | Scikit-learn, Pandas, NumPy |
| NLP | BERT / DistilBERT, NLTK, Transformers |
| Database | SQLite / MongoDB |
| Deployment | Vercel (Frontend), Render / Railway (Backend) |

---

## ⚙️ Installation & Setup  

### 🖥 Frontend
```bash
cd frontend
npm install
npm start
```

### 🧩 Backend
```bash
cd backend
pip install -r requirements.txt
uvicorn main:app --reload
```

Then open [http://localhost:5173](http://localhost:5173) and start exploring!

---

## 👨‍💻 Developer  

**Shashank Dadhich**  
AI/ML Developer | Building for Human Well-being 🌿  
🔗 [LinkedIn](https://www.linkedin.com/in/shashank-dadhich-b61880210/)  
🔗 [GitHub](https://github.com/shaa18)  

© 2025 Shashank Dadhich. All rights reserved.  

---

## 🧾 License  
Open-source under the **MIT License**.

---

## 🧠 Keywords  
`AI` `Machine Learning` `Burnout Detection` `Wellness Assistant` `Mental Health AI` `FastAPI` `React.js` `AIML Final Year Project` `Shashank Dadhich`
