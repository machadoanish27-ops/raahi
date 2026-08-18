# 🚌 Raahi — Smart Commuting Assistant

<p align="center">
  <strong>Smarter • Safer • Cleaner Daily Travel</strong>
</p>

<p align="center">
  A smart commuting platform that combines route intelligence, fare estimation,
  air-quality awareness, trip tracking, and sustainability insights into one experience.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.12-blue" alt="Python">
  <img src="https://img.shields.io/badge/Flask-3.0.3-black" alt="Flask">
  <img src="https://img.shields.io/badge/PostgreSQL-Database-336791" alt="PostgreSQL">
  <img src="https://img.shields.io/badge/Machine%20Learning-Optional-orange" alt="Machine Learning">
  <img src="https://img.shields.io/badge/Deployment-Vercel-black" alt="Vercel">
  <img src="https://img.shields.io/badge/License-MIT-green" alt="License">
</p>

---

## 🌍 Overview

**Raahi** is a smart commuting assistant designed to help users make better public-transportation decisions by bringing multiple commuting factors together in one platform.

Instead of looking at route information, transportation costs, air quality, travel history, and environmental impact separately, Raahi combines these inputs to provide practical commuting insights.

The platform helps users evaluate transportation options based on factors such as:

- 🕒 Travel time
- 💰 Estimated fare
- 🌫️ Air quality
- 🌱 CO₂ impact
- 📍 Route information
- 📊 Personal travel history

The goal is simple:

> **Help people travel smarter without needing to understand maps APIs, air-quality systems, or machine-learning models.**

---

# 🚨 The Problem

Everyday commuters make small transportation decisions that affect:

- Time
- Money
- Comfort
- Pollution exposure
- Environmental impact

A commuter may need to decide:

> Should I walk, take a train, use a bus, or take an auto?

Traditional route-planning solutions often focus primarily on distance or travel time.

Raahi takes a broader approach by combining **route, cost, air-quality, and sustainability information** into the commuting decision.

---

# 💡 The Solution

Raahi provides a centralized commuting platform where users can:

1. Enter a destination.
2. Compare available transportation options.
3. Evaluate estimated time and cost.
4. Understand AQI conditions.
5. Compare environmental impact.
6. Select a suitable route.
7. Track completed trips.
8. Monitor personal commuting insights.

---

# ✨ Key Features

## 🗺️ Smart Route Planner

Raahi compares multiple transportation modes for a destination, including:

- 🚶 Walking
- 🚆 Train
- 🚌 Bus
- 🚕 Auto

The system provides useful commuting information such as:

- Route distance
- Estimated travel time
- Estimated fare
- CO₂ impact

This allows users to compare transportation choices rather than relying on a single route.

---

## 💰 Fare Intelligence

Transportation cost is an important part of everyday commuting.

Raahi provides estimated fare information so users can compare different travel options and make more economical transportation decisions.

---

## 🌫️ AQI-Aware Commuting

Raahi incorporates air-quality information into the commuting experience.

Instead of considering only:

> "Which route is faster?"

users can also consider:

> "What are the air-quality conditions?"

This adds an environmental and health-awareness dimension to route selection.

---

## 🌱 CO₂ & Sustainability Insights

Raahi tracks the environmental impact of commuting choices.

Users can understand:

- CO₂ impact of trips
- CO₂ saved
- Money saved
- Travel history

This makes sustainable commuting measurable instead of invisible.

---

## 📊 Personal Profile Dashboard

The user dashboard provides a centralized view of commuting activity.

Users can track:

- Completed trips
- Travel history
- Money saved
- CO₂ saved
- Personal commuting information

---

## 📍 Location Support

Raahi supports saved user-location information to make route planning more personalized and convenient.

---

# 👨‍💼 Admin Features

Raahi also provides an administrative layer for monitoring and analyzing platform activity.

### Admin Dashboard

Provides an overview of:

- Registered users
- Trips
- Route activity
- AQI summaries
- Platform usage

### 👥 User Management

Administrators can view and manage registered users.

### 📈 Analytics

The platform supports structured analytics information for reviewing:

- User activity
- Trip activity
- Route usage
- AQI patterns

### 📤 Analytics Export

Analytics data can be prepared in a structured format for reporting and review.

### 🤖 Model Metrics

Where supported, administrators can view available machine-learning/model metrics to provide visibility into optional ML functionality.

---

# 🧠 Machine Learning Layer

Raahi includes an optional machine-learning layer inside:

```text
raahi_ml/
```

The ML component provides:

- Model pipelines
- Model helpers
- Optional advisory functionality
- Model-related metrics

The ML layer is designed to remain separate from the lightweight production application so that heavier machine-learning dependencies do not unnecessarily increase the production deployment footprint.

---

# 🏗️ System Architecture

```text
                        ┌──────────────────────┐
                        │        USER          │
                        │   Web Application    │
                        └──────────┬───────────┘
                                   │
                                   ▼
                        ┌──────────────────────┐
                        │      FRONTEND        │
                        │ HTML / CSS / JS      │
                        │ Jinja Templates      │
                        └──────────┬───────────┘
                                   │
                                   ▼
                        ┌──────────────────────┐
                        │    FLASK BACKEND     │
                        │                      │
                        │ Authentication       │
                        │ Route Intelligence   │
                        │ Fare Estimation      │
                        │ AQI Integration      │
                        │ Trip Management      │
                        │ Admin Features       │
                        │ ML Endpoints         │
                        └───────┬───────┬──────┘
                                │       │
                    ┌───────────┘       └────────────┐
                    ▼                                ▼
          ┌──────────────────┐              ┌──────────────────┐
          │    PostgreSQL    │              │   ML COMPONENT   │
          │     Database     │              │    raahi_ml/     │
          └──────────────────┘              └──────────────────┘
```

---

# 🔄 How Raahi Works

```text
                 Enter Destination
                         │
                         ▼
                Route Processing
                         │
             ┌───────────┼───────────┐
             │           │           │
             ▼           ▼           ▼
          Distance      Fare        AQI
             │           │           │
             └───────────┼───────────┘
                         │
                         ▼
                    CO₂ Analysis
                         │
                         ▼
                Compare Transport
                     Options
                         │
                         ▼
                   Choose Route
                         │
                         ▼
                    Track Trip
                         │
                         ▼
                Personal Dashboard
```

---

# 🛠️ Technology Stack

## Backend

- **Python**
- **Flask**
- **Flask-Login**
- **Flask-SQLAlchemy**
- **SQLAlchemy**

## Database

- **PostgreSQL**

## Frontend

- **HTML**
- **CSS**
- **JavaScript**
- **Jinja Templates**

## Machine Learning

- Python-based ML pipelines
- Optional model advisory components
- Model metrics

## Infrastructure & Deployment

- **Docker**
- **Docker Compose**
- **Vercel**
- PostgreSQL

---

# 📂 Project Structure

```text
Raahi/
│
├── backend/
│   ├── routes/
│   ├── services/
│   ├── models/
│   └── ...
│
├── frontend/
│   ├── templates/
│   └── static/
│
├── raahi_ml/
│   ├── models/
│   └── ...
│
├── config/
│
├── scripts/
│
├── tests/
│
├── .env.example
├── .gitignore
├── .vercelignore
├── CONTRIBUTING.md
├── docker-compose.yml
├── ISSUES_TO_FIX.md
├── LICENSE
├── pyproject.toml
├── requirements.txt
└── README.md
```

---

# ⚙️ Getting Started

## Prerequisites

Make sure the following are installed:

- Python 3.12+
- PostgreSQL
- Git
- Docker & Docker Compose *(optional)*

---

## 1️⃣ Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/raahi.git
cd raahi
```

---

## 2️⃣ Create a Python Virtual Environment

### Windows

```powershell
python -m venv .venv
```

Activate it:

```powershell
.\.venv\Scripts\Activate.ps1
```

### macOS / Linux

```bash
python3 -m venv .venv
source .venv/bin/activate
```

---

## 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 4️⃣ Configure Environment Variables

Create a local `.env` file from the provided example.

### Windows

```powershell
copy .env.example .env
```

### macOS / Linux

```bash
cp .env.example .env
```

Then open `.env` and configure the required values for:

- Database connection
- Authentication
- External APIs
- Application configuration
- Other required services

> ⚠️ **Never commit `.env` to GitHub.**

Only `.env.example` should be included in the repository.

---

## 5️⃣ Start the Application

Run the Flask application using:

```bash
python -m backend.main
```

The application serves the frontend through the Flask/Jinja application structure.

---

# 🐳 Docker Setup

Raahi includes Docker configuration for local development.

Build and start the services:

```bash
docker compose up --build
```

Stop the services:

```bash
docker compose down
```

---

# 🧪 Testing

The repository includes a dedicated test directory:

```text
tests/
```

Run the available test suite according to the project's configured testing setup.

Example:

```bash
pytest
```

> The exact test commands may depend on the configured environment and available services.

---

# 🔐 Security & Environment Variables

Raahi uses environment-based configuration to keep sensitive information outside the source code.

Never commit:

```text
.env
```

or any file containing:

```text
❌ Database passwords
❌ API keys
❌ API secrets
❌ Authentication secrets
❌ Private keys
❌ Production credentials
```

Use:

```text
.env.example
```

as the configuration template.

---

# 🌐 Deployment

Raahi includes configuration for **Vercel deployment**.

### Live Application

```text
https://raahi-wine.vercel.app
```

> The live deployment should be verified before relying on it as the production demonstration.

---

# 📸 Screenshots

Screenshots can be added to this section as the project presentation is expanded.

Recommended screenshots:

```text
screenshots/
├── landing-page.png
├── route-planner.png
├── route-results.png
├── aqi-information.png
├── user-dashboard.png
├── trip-history.png
└── admin-dashboard.png
```

Once added, they can be displayed here using:

```markdown
![Raahi Landing Page](screenshots/landing-page.png)

![Route Planner](screenshots/route-planner.png)

![Route Results](screenshots/route-results.png)

![User Dashboard](screenshots/user-dashboard.png)

![Admin Dashboard](screenshots/admin-dashboard.png)
```

---

# 📊 Example Decision Flow

Raahi is designed around a multi-factor commuting decision rather than a single "fastest route" recommendation.

```text
                ┌───────────────┐
                │  Destination  │
                └───────┬───────┘
                        │
                        ▼
              ┌───────────────────┐
              │ Available Routes  │
              └─────────┬─────────┘
                        │
         ┌──────────────┼──────────────┐
         ▼              ▼              ▼
      Time           Cost            AQI
         │              │              │
         └──────────────┼──────────────┘
                        ▼
                    CO₂ Impact
                        │
                        ▼
              ┌───────────────────┐
              │ Compare Options   │
              └─────────┬─────────┘
                        │
                        ▼
                  User Decision
```

---

# 🧩 Project Refinements

## 1. Cleaner Commuter Experience

Raahi keeps the commuter flow simple:

```text
Destination → Compare → Understand → Choose
```

The interface focuses on practical outputs instead of exposing unnecessary technical complexity.

---

## 2. AQI-Aware Route Planning

Route selection is not limited to speed.

Raahi adds air-quality context so users can consider:

- Pollution exposure
- Comfort
- Sustainability
- Travel conditions

---

## 3. Personal Impact Tracking

Completed trips are converted into measurable personal insights.

Users can understand:

- Trips completed
- Money saved
- CO₂ saved
- Travel history

---

## 4. Admin Intelligence

The administrative layer provides a higher-level view of:

- Users
- Trips
- Routes
- AQI
- Analytics
- Model availability

---

## 5. Lightweight Production Architecture

Raahi separates optional machine-learning components from the lightweight production application.

This allows heavier ML experimentation to remain separate from the deployment-oriented application layer.

---

# 🗺️ Supported Commuting Modes

Raahi is designed to compare common transportation options such as:

| Mode | Primary Considerations |
|---|---|
| 🚶 Walking | Distance, time, CO₂ |
| 🚆 Train | Time, fare, route |
| 🚌 Bus | Time, fare, route |
| 🚕 Auto | Time, fare, route |

---

# 📈 Sustainability

Raahi aims to make sustainable commuting choices measurable.

The platform can use commuting information to surface:

- CO₂ impact
- CO₂ saved
- Money saved
- Trip history
- Transportation comparisons

This helps users understand the impact of everyday transportation decisions.

---

# 🔮 Future Scope

Potential future improvements include:

### 🤖 Smarter Recommendations

- Personalized commuting recommendations
- Improved ML-based route intelligence
- User-specific travel preferences

### 🚆 Real-Time Transportation

- Live public transportation information
- Real-time delays
- Service availability
- Dynamic route updates

### 🌱 Advanced Sustainability

- More detailed emissions estimation
- Personal sustainability scores
- Long-term environmental analytics

### 📱 Mobile Experience

- Dedicated Android/iOS application
- Location-aware notifications
- Mobile-first trip tracking

### 📊 Advanced Analytics

- Historical commuting trends
- Predictive travel insights
- Advanced admin dashboards

---

# 🐛 Known Issues

See:

```text
ISSUES_TO_FIX.md
```

for known project issues and planned fixes.

---

# 🤝 Contributing

Contributions and improvements are welcome.

Please read:

```text
CONTRIBUTING.md
```

before submitting changes.

---

# 👥 Team Project

Raahi was developed as a **collaborative group project**.

This repository is my personal copy of the project maintained for **portfolio and documentation purposes**.

## 👨‍💻 My Contributions

> Replace the following placeholders with your **actual contributions** before publishing.

- [Contribution 1]
- [Contribution 2]
- [Contribution 3]

Examples of contribution categories could include:

- Frontend development
- Backend/API development
- Database integration
- Route/fare logic
- AQI integration
- ML components
- Dashboard development
- Testing
- Deployment

**Only list work you personally completed.**

## 👥 Team Members

Add the actual team members and their GitHub profiles here.

```text
- Team Member 1 — GitHub: https://github.com/username
- Team Member 2 — GitHub: https://github.com/username
- Team Member 3 — GitHub: https://github.com/username
```

---

# 📚 Project Documentation

Additional project documentation can be found in:

```text
CONTRIBUTING.md
ISSUES_TO_FIX.md
LICENSE
```

---

# 📄 License

This project is licensed under the **MIT License**.

See the [`LICENSE`](LICENSE) file for details.

---

# 🌱 Vision

> **Make everyday commuting simpler, smarter, and more sustainable.**

Raahi brings together **route, cost, air-quality, trip, and environmental information** to help commuters make better transportation decisions.

---

<p align="center">
  Built with ❤️ for smarter and more sustainable mobility.
</p>