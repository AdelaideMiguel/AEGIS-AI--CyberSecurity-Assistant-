 🛡️ AEGIS AI — AI Cybersecurity Assistant

AEGIS AI is an AI cybersecurity assistant designed to help users identify, understand, and respond to common digital security threats through a unified and user-friendly platform.

The project combines Artificial Intelligence, rule-based security analysis, threat assessment, security monitoring, and cybersecurity education to provide practical protection and awareness against everyday digital threats.



🚀 Features

### 🤖 AI Cybersecurity Assistant

Ask cybersecurity-related questions and receive intelligent guidance about phishing, scams, passwords, QR codes, application permissions, and other security risks.

### 🎣 Phishing Detection

Analyzes URLs and checks for potentially malicious or socially engineered websites using security intelligence.

### 💬 Message Scanner

Detects suspicious patterns in messages, including:

* Urgency and pressure tactics
* Requests for sensitive information
* Prize and giveaway scams
* Impersonation attempts
* Suspicious URLs
* URL shorteners and obfuscation
* Excessive punctuation

### 🔐 Password Security Analyzer

Evaluates password strength based on:

* Password length
* Uppercase and lowercase characters
* Numbers
* Special characters
* Common password patterns
* Repeated patterns

The password is analyzed locally and is **not stored or transmitted**.

### 📷 QR Code Scanner

Uses the device camera to scan QR codes and identify their content, including potentially unsafe links.

### 📱 Application Permission Analyzer

Examines installed applications and identifies potentially risky permissions such as:

* SMS
* Contacts
* Camera
* Microphone
* Location
* Phone
* Storage
* Notifications

### 🚨 Threat Monitoring

Provides a centralized dashboard for viewing detected threats and their severity.

Threat levels include:

**SAFE → LOW → MEDIUM → HIGH → CRITICAL**

### 📊 Security Score

The dashboard calculates an overall security score based on active threats and identified permission risks, helping users quickly understand their current security condition.

### 📚 Security Education

Provides educational content about:

* Phishing
* Password security
* QR-code safety
* SMS scams
* Social engineering
* Public Wi-Fi
* Application permissions
* Multi-factor authentication

### 📈 Security History & Reports

Stores security events locally and provides historical information and reports for reviewing previous security activity.

---

# 🏗️ System Architecture

```text
                ┌──────────────────────┐
                │      AEGIS AI        │
                │   Android Client     │
                └──────────┬───────────┘
                           │
              ┌────────────┴────────────┐
              │                         │
       Local Analysis             Backend Services
              │                         │
      ┌───────┼────────┐          ┌─────┴─────────┐
      │       │        │          │               │
   Message  Password  Permissions Cloudflare   External
   Scanner  Analyzer   Analyzer    Worker      Security
                                      │          Intelligence
                                      │
                              ┌───────┴────────┐
                              │                │
                         Google Gemini    Google Web Risk
```

---

# 🛠️ Technology Stack

## Android Application

* **Kotlin**
* **Jetpack Compose**
* **Material 3**
* **Android Architecture Components**
* **Navigation Compose**
* **Coroutines**
* **CameraX**
* **Google ML Kit**

## Local Storage

* **Room Database**
* **DataStore Preferences**

## Backend

* **Cloudflare Workers**
* **REST API**
* **OkHttp**

## AI & Security Intelligence

* **Google Gemini**
* **Google Web Risk**

---

# 🔄 Application Workflow

```text
User Input
    ↓
Security Module
    ↓
Threat / Risk Analysis
    ↓
Severity Classification
    ↓
Security Recommendation
    ↓
Dashboard & History
```

Different modules use different approaches depending on the task.

Local security analysis is used where possible, while backend services provide AI assistance and external URL security intelligence.

---

# 📊 Security Scoring

AEGIS AI uses different scoring mechanisms for different modules.

### Overall Security Score

The dashboard starts with a score of **100** and applies penalties for active threats and permission risks.

| Risk Level | Penalty |
| ---------- | ------- |
| Critical   | -15     |
| High       | -8      |
| Medium     | -4      |
| Low        | -1      |
| Safe       | 0       |

The final score is limited between **0 and 100**.

### Message Scanner

The Message Scanner uses a suspicion score based on detected scam indicators.

| Score | Risk     |
| ----: | -------- |
|     0 | Safe     |
|     1 | Low      |
|   2–3 | Medium   |
|   4–5 | High     |
|    6+ | Critical |

### Password Analyzer

Password strength is represented using a **0–100 score** and categorized as:

|  Score | Strength    |
| -----: | ----------- |
| 85–100 | Very Strong |
|  65–84 | Strong      |
|  45–64 | Moderate    |
|  20–44 | Weak        |
|   0–19 | Very Weak   |

---

# 🔒 Security & Privacy

AEGIS AI follows a security-conscious design approach.

* Password analysis is performed locally.
* Passwords are not stored in the application database.
* Sensitive application secrets are not included in the public source code.
* The Android application communicates with the backend through authenticated requests.
* The application avoids unnecessary access to private device content.
* Android's permission system is used for security-sensitive functionality.

**Never commit API keys, service-account credentials, passwords, or application secrets to GitHub.**

---

# 📱 Main Modules

```text
Home Dashboard
│
├── AI Assistant
├── Threat Detection
├── Phishing Detector
├── Message Scanner
├── Password Analyzer
├── QR Scanner
├── Permission Analyzer
├── Security Tools
├── Security Education
├── Threat History
├── Reports
└── Settings
```

---

# ⚠️ Current Limitations

The current project is an academic cybersecurity prototype.

The Threat Scanner currently uses **simulated security findings** rather than continuously inspecting live network traffic or complete device telemetry.

Threat management actions such as blocking or dismissing threats are currently maintained within the application's local database and do not directly block network connections.

These components provide a foundation for future real-time security integrations.

---

# 🔮 Future Scope

Future versions of AEGIS AI could include:

* Real-time network traffic monitoring
* Machine-learning-based intrusion detection
* Behavioral threat analysis
* Advanced anomaly detection
* Continuous security monitoring
* Expanded threat intelligence
* Automated incident response
* Cloud-based security analytics
* Advanced phishing classification
* Real-time notification and alert systems

---

# 🎯 Project Objective

The main objective of AEGIS AI is to demonstrate how **Artificial Intelligence and cybersecurity technologies can be combined to create an accessible and proactive security assistant**.

The project aims to help users detect potential threats, understand cybersecurity risks, and make safer decisions when interacting with digital content and applications.

---

# 👩‍💻 Project Information

**Project Name:** AEGIS AI — AI-Powered Cybersecurity Assistant
**Domain:** Artificial Intelligence & Cybersecurity
**Platform:** Android
**Academic Year:** 2026–2027

**Developed using:** Kotlin, Jetpack Compose, Cloudflare Workers, Google Gemini, Google Web Risk, Room Database, CameraX, and Google ML Kit.

---

# 📄 License

This project was developed as an academic project for educational and demonstration purposes.

---

## 🛡️ AEGIS AI

> **Understand the threat. Assess the risk. Stay protected.**
