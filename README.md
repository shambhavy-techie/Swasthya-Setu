# 🏥 Swasthya Setu

### स्वास्थ्य सेतु — स्वास्थ्य भारत, सुरक्षित भारत
**Connecting Patients, Doctors & Healthcare Across India**

Swasthya Setu is a bilingual hospital patient-assistance and appointment-booking prototype built with Python and Streamlit. The project aims to simplify the patient journey by bringing registration, health-concern selection, doctor discovery, appointment-slot selection, token generation, and appointment-document generation into one guided digital workflow.

---

## 1. 📌 Project Overview

Patients can often face unnecessary complexity when they visit government hospitals without prior appointment, finding the appropriate specialist, understanding where to go, and keeping track of appointment information.

**Swasthya Setu** addresses this by providing a simple step-by-step digital interface that guides a patient from registration to appointment confirmation.

The prototype supports:

- Hindi and English interaction
- Patient registration
- Disease/problem selection
- Text and voice-based problem description
- Emergency-mode demonstration
- Hospital and specialist selection
- Appointment-slot selection
- Automatic token generation
- Appointment PDF generation
- Optional temporary-care guidance
- Consistent Swasthya Setu branding and an animated introduction

---

## 2. ❗ Problem Statement

Government Hospital lacks appointment processes and there can be a huge rush, confusing and time-consuming, particularly for patients who may have difficulty navigating multiple steps or communicating their health concern.

There is a need for a **simple, accessible and patient-friendly digital system** that can:

1. Collect essential patient information in a guided manner.
2. Allow patients to communicate their health concern using text or voice.
3. Help connect the selected health concern with an appropriate medical specialization.
4. Show available doctors and appointment slots in a structured way.
5. Provide a clear token number and appointment record after booking.
6. Support both Hindi and English to improve accessibility.
7. Present emergency assistance as a clearly separated workflow.

**Swasthya Setu** is designed as a prototype solution to demonstrate this patient journey in a single interface.

---

## 3. ✨ Features

### 👤 Patient Registration
Collects basic patient information such as name, age, gender, contact number and city.

### 🌐 Bilingual Interface
Patients can choose between **Hindi and English**.

### 🩺 Health Concern Selection
Provides a structured list of common diseases and health concerns, including fever, flu, asthma, diabetes, high blood pressure, heart disease, migraine, skin allergy, eye infection, ear infection, UTI and others.

### 🎙️ Voice Input
The patient can use the microphone to describe their problem instead of typing it manually.

### 🚨 Emergency Mode
Provides a separate emergency demonstration flow with an emergency alert interface which connects to the ambulance of nearest government hospital.

### 👨‍⚕️ Doctor & Specialist Selection
The selected health concern is used to determine relevant medical specializations, after which suitable doctors and their details are fetched using AI and are displayed.

### 📅 Appointment Slot Booking
Patients can select an available appointment slot and book it.

### 🎫 Automatic Token Generation
A token number is generated after successful booking and displayed on the confirmation screen.

### 📄 Appointment PDF
The patient can download a PDF containing their appointment information.

### 🤖 Temporary-Care Guidance
After booking, the prototype can display conservative temporary-care information using AI related to the selected health concern, along with a warning to seek appropriate medical care.

### 🎨 Swasthya Setu Branding
The application begins with an animated Swasthya Setu introduction and displays the project logo on the application's pages.

---

## 4. 🤖 AI / Intelligent Component

The prototype includes an **AI-oriented patient-assistance workflow**.

The current version uses a structured, rule-based mapping between the selected health concern and relevant medical specializations, followed by personalized doctor/slot presentation. It also provides disease-specific temporary-care guidance.

---

## 5. 🛠️ Technology Stack

- **Python 3**
- **Streamlit** — interactive web application
- **SpeechRecognition** — voice input
- **ReportLab** — PDF appointment generation
- **Base64 / embedded assets** — logo and intro artwork
- **Streamlit Session State** — multi-step patient workflow

---

## 6. 📁 Project Structure

```text
Swasthya-Setu/
│
├── Swasthya Setu.py
└── README.md
```

The current application embeds the Swasthya Setu logo/intro artwork directly inside the Python source, so a separate logo file is not required for the current version.

---

## 7. ⚙️ Setup / Installation

### Prerequisites

Install:

- Python 3
- VS Code (recommended for development)

### Step 1 — Clone or download the repository

If using Git:

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd Swasthya-Setu
```

Alternatively, download the repository ZIP from GitHub and extract it.

### Step 2 — Install dependencies

Open a terminal in the project folder and run:

```bash
pip install streamlit SpeechRecognition reportlab
```

The voice-input feature requires microphone/audio support. Depending on the operating system, an additional audio dependency such as `PyAudio` may be required.

### Step 3 — Run the application

Run:

```bash
streamlit run "Swasthya Setu.py"
```

The terminal will provide a local address, normally:

```text
http://localhost:8501
```

Open this address in a web browser.

---

## 8. ▶️ Usage Instructions

### Step 1 — Launch
Run the Streamlit command above. The animated Swasthya Setu introduction appears first.

### Step 2 — Select Language
Choose:

- 🇮🇳 Hindi
- 🌐 English

### Step 3 — Enter Patient Information
Enter the requested personal information and select the city.

### Step 4 — Select Health Concern
Choose the relevant disease/problem or enter the emergency workflow if necessary.

### Step 5 — Describe the Problem
Type the problem or use the microphone button to provide a voice description.

### Step 6 — View Hospital & Doctors
The application processes the selected health concern and presents the corresponding hospital, specialists and doctors.

### Step 7 — Select Appointment Slot
Choose a doctor and an available appointment slot.

### Step 8 — Receive Token
After booking, the application generates and displays the patient's token number and appointment details.

### Step 9 — Download Appointment PDF
Use the download button to save the appointment record as a PDF.

### Step 10 — Optional Temporary Guidance
The patient can open the temporary-care guidance section for conservative information intended only for the period before the hospital appointment.

---

## 9. 🔄 Complete Patient Flow

```text
Animated Introduction
        ↓
Language Selection
        ↓
Patient Registration
        ↓
Health Concern / Emergency
        ↓
Problem Description
        ↓
Voice or Text Input
        ↓
Processing
        ↓
Hospital + Specialist Doctors
        ↓
Appointment Slot
        ↓
Booking Confirmation
        ↓
Token Number
        ↓
Appointment PDF
        ↓
Optional Temporary Guidance
```

---

## 10. 📄 Appointment Record

After successful booking, the application displays:

- Patient name
- Disease / health concern
- Doctor
- Specialization
- Hospital floor
- Cabin
- Appointment time
- Assigned token number

The appointment information can then be downloaded as a PDF.

---

## 11. ⚠️ Prototype Limitations

This is a working prototype rather than a production hospital-management system.

- Hospital and doctor information is stored in the application rather than being retrieved from a live hospital database.
- Appointment slots are prototype data and do not create a real hospital appointment.
- Patient information is handled through the Streamlit session and is not connected to a production electronic health-record system.
- The emergency workflow is a demonstration and should not be treated as a real emergency-dispatch service.
- Temporary-care guidance is not a medical diagnosis or treatment plan.

---

## 12. 🔐 Privacy & Safety

Do not use real patient medical information while demonstrating or testing the prototype.

Never commit passwords, API keys, authentication tokens, or other secrets to the public GitHub repository.

---

## 13. 🎯 Project Goal

The goal of Swasthya Setu is to demonstrate how a patient-friendly digital interface can simplify the hospital journey:

**Register → Describe → Find the right specialist → Choose a slot → Receive a token → Get an appointment record**

The project emphasizes accessibility, bilingual interaction, guided navigation and a simplified patient experience.

---

## 14. 👥 Project Information

**Project:** Swasthya Setu  
**Category:** Healthcare / Digital Health  
**Application Type:** Patient Registration & Appointment Prototype  
**Built With:** Python + Streamlit

---

## 15. 📌 GitHub Submission Checklist

Before submitting the repository, make sure it contains:

- [ ] `Swasthya Setu.py`
- [ ] `README.md`
- [ ] Clear project overview
- [ ] Problem statement
- [ ] Features
- [ ] Setup/installation instructions
- [ ] Usage instructions
- [ ] Public GitHub repository
- [ ] Meaningful Git commit history
- [ ] No passwords, API keys or private information

### Important for evaluation

The repository should remain **Public throughout the evaluation process**, as required by the competition.

---

**Swasthya Setu — स्वास्थ्य भारत, सुरक्षित भारत 🇮🇳🏥**
