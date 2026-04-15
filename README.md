 #  my project # 
 
 # 🕷️ SPYDER - Smart Police Intelligence System
# Smart Police Yielding Digital Evidence & Response

> AI-Powered Public Safety Platform | Hackathon Project 2024

---

## 🎯 Project Overview

SPYDER is a full-stack AI-powered smart policing web application built with Python (Flask) for backend and HTML/CSS/JavaScript for frontend. It connects police officers and citizens through a digital platform to improve crime detection, ensure women safety, and help track missing persons.

---

## ✨ Features

### 🔐 Authentication
- Separate login portals for **Police Officers** and **Citizens**
- Spider crawl animation on intro page
- Secure session management

### 👮 Police Dashboard
- **Live Alerts Feed** - Real-time notifications
- **AI Face Detection** - Criminal/Missing person detection simulation
- **FIR Management** - File, view, update FIR status
- **Complaint Management** - All public complaints
- **Missing Persons DB** - Track and update cases
- **Women Safety Monitoring** - Live SOS alerts
- **Cyber Crime Cases** - Harassment reports with repeat offender detection
- **Crime Map** - Leaflet.js with crime heatmap (Hyderabad)
- **Crime Prediction** - AI analysis of crime patterns

### 👤 Citizen Dashboard
- **SOS Emergency Button** - One-tap alert with GPS
- **File Complaint** - Multiple crime types
- **File FIR Online** - Digital FIR submission
- **Report Missing Person** - With description
- **Cyber Harassment** - Report with platform ID
- **Voice Trigger Detection** - Detects "Help me", "Save me" etc. using Web Speech API
- **Live Location Map** - Share location with police
- **Track Complaints** - Status tracking

---

## 🛠️ Setup Instructions

### Step 1: Install Python
Make sure Python 3.8+ is installed.

```bash
python --version
```

### Step 2: Install Dependencies

```bash
pip install flask
pip install opencv-python
pip install SpeechRecognition
pip install pyaudio
pip install numpy
```

Or install all at once:
```bash
pip install -r requirements.txt
```

> **Note for Windows**: If pyaudio fails, install via:
> ```
> pip install pipwin
> pipwin install pyaudio
> ```

### Step 3: Project Structure

```
spyder/
├── app.py                  ← Main Flask application
├── requirements.txt        ← Dependencies
├── spyder.db              ← SQLite database (auto-created)
├── evidence/              ← Evidence photos saved here
├── uploads/               ← Uploaded images
├── criminal_db/           ← Criminal face photos
├── missing_db/            ← Missing person photos
└── templates/
    ├── intro.html         ← Spider animation intro page
    ├── login_police.html  ← Police login
    ├── login_public.html  ← Citizen login
    ├── police_dashboard.html ← Police command center
    └── public_dashboard.html ← Citizen safety portal
```

### Step 4: Run the Application

```bash
cd spyder
python app.py
```

You'll see:
```
╔══════════════════════════════════════════╗
║   🕷️  SPYDER - Smart Police System       ║
║   Starting on http://localhost:5000      ║
║                                          ║
║   Police Login: officer001 / police123   ║
║   Public Login: citizen001 / public123   ║
╚══════════════════════════════════════════╝
```

### Step 5: Access the Application

Open your browser and go to: **http://localhost:5000**

---

## 🔑 Login Credentials

### Police Officers
| Username | Password | Role |
|----------|----------|------|
| officer001 | police123 | Inspector Ravi Kumar |
| officer002 | police123 | Sub-Inspector Priya |

### Citizens
| Username | Password | Role |
|----------|----------|------|
| citizen001 | public123 | Citizen |

---

## 📱 Mobile Camera Integration (IP Webcam)

1. Install **IP Webcam** app on your Android phone
2. Start the server in the app
3. Note the IP address (e.g., `192.168.1.100:8080`)
4. Update `CAMERA_URL` in `app.py`:
   ```python
   CAMERA_URL = "http://YOUR_PHONE_IP:8080/video"
   ```

---

## 🧠 AI Face Recognition Setup (Advanced)

To enable real face recognition:

1. Install additional packages:
   ```bash
   pip install face-recognition
   pip install cmake
   pip install dlib
   ```

2. Add criminal photos to `criminal_db/` folder
3. Add missing person photos to `missing_db/` folder
4. Run training script: `python train.py`
5. Start detection from Police Dashboard

---

## 🗺️ Crime Map

- Uses **Leaflet.js** + **OpenStreetMap** (free, no API key needed)
- Shows crime incidents around **Hyderabad, Telangana**
- Color coding: 🔴 High | 🟡 Medium | 🟢 Low

---

## 📊 Database Tables

| Table | Purpose |
|-------|---------|
| users | Police officers & citizens |
| firs | First Information Reports |
| complaints | Public complaints |
| missing_persons | Missing person reports |
| cyber_harassment | Online harassment cases |
| alerts | System notifications |
| crime_incidents | Map data points |
| sos_alerts | Emergency SOS records |

---

## 🚺 Women Safety Features

1. **SOS Button** - One-click emergency alert
2. **Voice Trigger** - Detects "Help me", "Save me", "Bachao" using browser Web Speech API
3. **Live Location** - GPS sharing with police
4. **Cyber Harassment** - Report with repeat offender detection

---

## 🔮 Crime Prediction

The AI analyzes:
- Time patterns (day/night crime ratio)
- Location frequency
- Crime type trends
- Historical FIR data

Outputs risk predictions for different areas and times.

---

## 🏆 Hackathon Highlights

- ✅ Real-world problem solving
- ✅ Full-stack implementation
- ✅ AI/ML integration
- ✅ Modern dark UI/UX
- ✅ Dual-role system (Police + Citizens)
- ✅ Live maps & crime analytics
- ✅ Voice recognition
- ✅ Mobile camera support
- ✅ Real-time alerts

---

## 📞 Emergency Numbers
- 🚔 Police: **100**
- 🚒 Fire: **101**  
- 🚑 Ambulance: **108**
- 👩 Women Helpline: **1091**

---

*Built with for public safety — SPYDER v2.0*
