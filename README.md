# 🛡️ AI-Powered Email Threat Detection, GeoLocation & Forensic Intelligence Platform

<p align="center">

**An AI-powered cybersecurity platform for detecting email threats, analyzing suspicious emails, identifying IP-based intelligence, and supporting digital forensic investigation.**

</p>

---

## 🚨 Problem Statement

Email-based cyber threats such as **phishing, spoofing, impersonation, malicious URLs, fraudulent messages, and social engineering attacks** are increasing rapidly.

Traditional email security solutions may detect suspicious emails, but investigators often need additional information such as:

* Is the email actually suspicious?
* What indicators make the email dangerous?
* Has the sender information been manipulated?
* What IP address or infrastructure is associated with the email?
* Where is the suspicious IP geographically located?
* What forensic evidence can be extracted from the email?

This project provides a **unified platform** that combines **AI-based threat detection, email header analysis, IP geolocation, and digital forensic intelligence**.

---

# 💡 Proposed Solution

Our platform analyzes an uploaded email and generates a comprehensive security assessment.

```text
                    📧 Suspicious Email
                           │
                           ▼
                  📋 Email Parser
                           │
             ┌─────────────┼─────────────┐
             ▼             ▼             ▼
        Email Headers   Email Body    URLs/Links
             │             │             │
             └─────────────┼─────────────┘
                           ▼
                  🤖 AI Threat Detection
                           │
                           ▼
                     Risk Scoring
                           │
              ┌────────────┼────────────┐
              ▼            ▼            ▼
             LOW         MEDIUM        HIGH
                           │
                           ▼
                  🔎 Forensic Analysis
                           │
                           ▼
                 🌍 IP GeoLocation
                           │
                           ▼
              🧠 Threat Intelligence
                           │
                           ▼
                  📊 Security Dashboard
                           │
                           ▼
                 📄 Forensic Report
```

---

# ✨ Key Features

## 1. 🤖 AI-Powered Threat Detection

The system analyzes email characteristics to identify potential threats.

* Phishing detection
* Suspicious keyword detection
* Malicious URL indicators
* Sender analysis
* Risk scoring
* Threat classification

---

## 2. 📧 Email Header Forensics

The platform extracts and analyzes important email headers such as:

* `From`
* `To`
* `Reply-To`
* `Return-Path`
* `Message-ID`
* `Date`
* Received headers

This helps identify potential spoofing and email-routing anomalies.

---

## 3. 🌍 IP Geolocation Intelligence

Suspicious IP addresses can be enriched with geographical and network information.

Information may include:

* IP Address
* Country
* Region
* City
* Latitude
* Longitude
* ISP / Organization
* ASN

> **Note:** IP geolocation provides approximate infrastructure/location information and should not be treated as proof of a person's physical location.

---

## 4. 🔎 Digital Forensic Analysis

The system extracts useful indicators from suspicious emails.

Examples:

* Sender and Reply-To mismatch
* Missing headers
* Suspicious URLs
* Suspicious keywords
* Email metadata
* Attachment metadata
* IP information
* Domain-related indicators

---

## 5. 📊 Risk Scoring

Each analyzed email receives a risk score from **0–100**.

|  Score | Risk Level |
| -----: | ---------- |
|   0–39 | 🟢 LOW     |
|  40–69 | 🟡 MEDIUM  |
| 70–100 | 🔴 HIGH    |

The score can be improved later using a trained machine-learning model.

---

# 🏗️ System Architecture

```text
                    ┌───────────────────┐
                    │   User / Analyst  │
                    └─────────┬─────────┘
                              │
                              ▼
                    ┌───────────────────┐
                    │ Web Dashboard     │
                    │ HTML/CSS/JS       │
                    └─────────┬─────────┘
                              │ REST API
                              ▼
                    ┌───────────────────┐
                    │ Flask Backend     │
                    └─────────┬─────────┘
                              │
          ┌───────────────────┼───────────────────┐
          ▼                   ▼                   ▼
 ┌────────────────┐  ┌────────────────┐  ┌────────────────┐
 │ Email Parser   │  │ AI Threat      │  │ Forensic       │
 │                │  │ Detection      │  │ Analyzer       │
 └───────┬────────┘  └───────┬────────┘  └───────┬────────┘
         │                   │                   │
         └───────────────────┼───────────────────┘
                             ▼
                    ┌───────────────────┐
                    │ IP Intelligence   │
                    │ & GeoLocation     │
                    └─────────┬─────────┘
                              │
                              ▼
                    ┌───────────────────┐
                    │ MySQL Database    │
                    └─────────┬─────────┘
                              │
                              ▼
                    ┌───────────────────┐
                    │ Threat Report /   │
                    │ Dashboard         │
                    └───────────────────┘
```

---

# 🛠️ Technology Stack

| Layer            | Technology            |
| ---------------- | --------------------- |
| Frontend         | HTML, CSS, JavaScript |
| Backend          | Python, Flask         |
| Database         | MySQL                 |
| Machine Learning | Python, Scikit-learn  |
| Data Processing  | Pandas, NumPy         |
| Email Processing | Python Email Library  |
| GeoLocation      | IP Intelligence API   |
| API              | REST API              |
| Development      | Visual Studio Code    |
| Version Control  | Git & GitHub          |

---

# 📁 Project Structure

```text
AI-Email-Threat-Detection-Forensic-Intelligence/
│
├── README.md
├── requirements.txt
├── .gitignore
├── LICENSE
│
├── backend/
│   ├── app.py
│   │
│   ├── routes/
│   │   ├── email_routes.py
│   │   ├── forensic_routes.py
│   │   └── geolocation_routes.py
│   │
│   ├── services/
│   │   ├── email_parser.py
│   │   ├── threat_detector.py
│   │   ├── geolocation.py
│   │   └── forensic_analyzer.py
│   │
│   └── models/
│       └── database.py
│
├── frontend/
│   ├── index.html
│   ├── css/
│   │   └── style.css
│   └── js/
│       └── app.js
│
├── database/
│   └── schema.sql
│
├── ml/
│   ├── train_model.py
│   ├── predict.py
│   ├── dataset/
│   └── model/
│
├── uploads/
│   └── .gitkeep
│
├── tests/
│   └── test_api.py
│
└── docs/
    ├── architecture.md
    └── API.md
```

---

# ⚙️ Installation & Setup

## 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/AI-Email-Threat-Detection-Forensic-Intelligence.git
```

```bash
cd AI-Email-Threat-Detection-Forensic-Intelligence
```

---

## 2. Create Virtual Environment

### Windows

```bash
python -m venv venv
```

Activate:

```bash
venv\Scripts\activate
```

### Linux / macOS

```bash
python3 -m venv venv
```

```bash
source venv/bin/activate
```

---

## 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

# 🗄️ MySQL Database Setup

Make sure MySQL is installed and running.

Open MySQL:

```bash
mysql -u root -p
```

Then execute:

```sql
SOURCE database/schema.sql;
```

The database contains tables for:

* Email analysis
* IP intelligence
* Forensic findings

---

# 🔐 Environment Variables

Create a `.env` file for sensitive configuration.

Example:

```env
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=your_password
DB_NAME=email_forensics

GEOLOCATION_API_KEY=your_api_key
```

**Never upload `.env` to GitHub.**

The `.gitignore` file should contain:

```text
.env
venv/
__pycache__/
uploads/*
```

---

# ▶️ Running the Backend

Navigate to the backend:

```bash
cd backend
```

Run Flask:

```bash
python app.py
```

The backend will run at:

```text
http://localhost:5000
```

Health check:

```text
GET /api/health
```

---

# 🌐 Running the Frontend

Open:

```text
frontend/index.html
```

in your browser.

Alternatively, if you are using VS Code, install **Live Server** and open the HTML file using Live Server.

---

# 🔌 API Endpoints

## Health Check

```http
GET /api/health
```

Example response:

```json
{
    "status": "healthy",
    "service": "email-threat-detection-api"
}
```

---

## Email Analysis

```http
POST /api/email/analyze
```

Upload:

```text
file = suspicious_email.eml
```

The API returns:

* Email headers
* Email body
* Attachments
* Risk score
* Risk level
* Suspicious keywords
* URL count

---

## IP Geolocation

```http
GET /api/geolocation/lookup?ip=8.8.8.8
```

Example response:

```json
{
    "ip": "8.8.8.8",
    "country": "United States",
    "region": "California",
    "city": "Mountain View",
    "latitude": 37.4056,
    "longitude": -122.0775
}
```

---

## Forensic Analysis

```http
POST /api/forensic/analyze
```

The endpoint analyzes available email metadata and returns potential forensic findings.

---

# 🤖 AI/ML Pipeline

The planned AI/ML pipeline is:

```text
              Email Dataset
                    ↓
              Data Cleaning
                    ↓
            Feature Extraction
                    ↓
           Feature Engineering
                    ↓
             Model Training
                    ↓
             Model Evaluation
                    ↓
          Threat Classification
                    ↓
              Risk Score
```

### Potential Features

* Email text
* URL count
* URL characteristics
* Sender domain
* Header anomalies
* Authentication results
* Attachment metadata
* IP/ASN intelligence
* Suspicious phrases

### Potential ML Models

* Logistic Regression
* Random Forest
* Support Vector Machine
* Gradient Boosting / XGBoost
* Transformer-based NLP models

The initial MVP may use a rule-based detector while the trained ML model is being developed.

---

# 🔍 Forensic Investigation Workflow

```text
1. Upload Email
       ↓
2. Parse Email
       ↓
3. Extract Headers
       ↓
4. Analyze Sender
       ↓
5. Analyze URLs
       ↓
6. Extract IP Addresses
       ↓
7. Perform IP Intelligence
       ↓
8. Detect Suspicious Indicators
       ↓
9. Calculate Risk Score
       ↓
10. Generate Investigation Report
```

---

# 📊 Expected Output

The dashboard can provide:

```text
┌─────────────────────────────────────┐
│        EMAIL THREAT ANALYSIS        │
├─────────────────────────────────────┤
│ Risk Score       : 82 / 100         │
│ Risk Level       : HIGH             │
│                                     │
│ Sender           : example@mail.com │
│ Subject          : Urgent Account   │
│                                     │
│ Suspicious URLs  : 3                │
│ Keywords         : 5                │
│                                     │
│ GeoLocation                           │
│ Country          : Unknown          │
│ Region           : Unknown          │
│ IP/ASN           : Available        │
│                                     │
│ ⚠ Potential phishing indicators     │
└─────────────────────────────────────┘
```

---

# 🎯 SIH MVP

The Minimum Viable Product includes:

* 📧 `.eml` email upload
* 📋 Email header extraction
* 🔎 Header forensic analysis
* 🔗 URL detection
* 🤖 Threat detection
* 📊 Risk scoring
* 🌍 IP geolocation
* 🗄️ MySQL database
* 🌐 Web dashboard
* 🔌 REST APIs
* 📄 Forensic findings

---

# 👥 Team Responsibilities

| Member   | Responsibility                    |
| -------- | --------------------------------- |
| Member 1 | MySQL Database + Backend          |
| Member 2 | AI/ML Model                       |
| Member 3 | Email Forensics                   |
| Member 4 | Frontend & UI/UX                  |
| Member 5 | GeoLocation & Threat Intelligence |
| Member 6 | Integration, Testing & Deployment |

---

# 🚀 Future Scope

Future versions can include:

* Advanced phishing detection
* SPF/DKIM/DMARC analysis
* Domain reputation analysis
* WHOIS intelligence
* Malicious URL reputation
* Attachment analysis
* Threat intelligence feeds
* Interactive world map
* Automated PDF forensic reports
* Explainable AI
* SIEM integration
* SOC dashboard
* Real-time email monitoring
* Advanced NLP/Transformer models

---

# 🔒 Security & Privacy

Security is a major consideration of this project.

The system should:

* Validate uploaded files
* Restrict upload size
* Sanitize user input
* Protect database credentials
* Secure API keys
* Avoid exposing sensitive information
* Keep private emails out of public repositories
* Maintain appropriate access controls
* Log security events securely

**Never upload real confidential emails or sensitive forensic evidence to this public GitHub repository.**

Use sanitized/sample `.eml` files for demonstration.

---

# 🧪 Testing

Run tests using:

```bash
pytest
```

API testing can also be performed using:

* Postman
* cURL
* Browser developer tools

---

# 📌 Project Status

```text
🟢 Frontend             → In Development
🟢 Flask Backend        → In Development
🟢 Email Parser         → Implemented
🟢 Basic Threat Engine  → Implemented
🟢 MySQL Database       → Implemented
🟡 GeoLocation          → Integration
🟡 AI/ML Model          → Development
🟡 Forensic Reporting   → Planned
```

---

# 🏆 Smart India Hackathon

This project is being developed as a **Smart India Hackathon (SIH)** project focused on cybersecurity, email threat detection, geolocation intelligence, and digital forensics.

The objective is to provide investigators and security analysts with a centralized platform for analyzing suspicious email evidence and generating actionable intelligence.

---

# ⚠️ Disclaimer

This project is intended for:

* Educational purposes
* Cybersecurity research
* Authorized security analysis
* Digital forensic investigation

Only analyze emails, systems, networks, and data for which you have appropriate authorization.

---

# 📜 License

This project is licensed under the **MIT License**.

---

# ⭐ Contributors

Developed by the SIH Team.

**AI-Powered Email Threat Detection, GeoLocation & Forensic Intelligence Platform**

⭐ If you find this project useful, consider giving the repository a star!
