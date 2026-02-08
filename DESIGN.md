# design.md — AI Bharat Sahayak

## 1. System Overview

AI Bharat Sahayak is a multilingual, voice-enabled web application that assists Indian citizens in understanding and accessing government schemes. The system follows a client–server architecture with AI-driven processing and cloud-based deployment.

Users interact with a web interface using either text or voice. The backend processes the input, understands the intent, retrieves relevant scheme information, and generates a clear response in the user's preferred language. The system then converts the response into speech if required.

---

## 2. High-Level Architecture

The system consists of the following components:

1. **User Interface (Frontend)**
   - Web application built using React.
   - Provides:
     - Text input box
     - Microphone button for voice input
     - Language selection dropdown
     - Chat display area

2. **Backend API Layer (FastAPI)**
   - Receives requests from frontend.
   - Coordinates:
     - Speech-to-text conversion
     - Intent detection
     - Data retrieval
     - Text generation
     - Text-to-speech conversion

3. **AI Processing Layer**
   - **Speech-to-Text (ASR):** Converts user voice into text using Indic-ASR.
   - **Intent Understanding (NLP/LLM):** Determines what the user is asking.
   - **Response Generator:** Produces simple, human-readable answers.

4. **Scheme Database**
   - Stores structured data about government schemes:
     - Description
     - Eligibility
     - Documents required
     - Application steps
     - Online/offline application details

5. **Cloud Infrastructure (AWS)**
   - Frontend hosted on AWS S3 + CloudFront.
   - Backend hosted on AWS EC2 Free Tier.
   - Secure communication via HTTPS.

---

## 3. Data Flow

### Step-by-step flow:

1. **User Input**
   - User speaks or types a question.

2. **Frontend Processing**
   - If voice: audio is captured.
   - If text: message is sent directly.

3. **Backend Processing**
   - Audio → converted to text (ASR).
   - Text is analyzed for intent.

4. **Data Retrieval**
   - Backend queries the scheme database.

5. **Response Generation**
   - AI generates a simple explanation.

6. **Text-to-Speech (Optional)**
   - Response converted to audio.

7. **Final Output**
   - Text and/or audio sent back to user.

---

## 4. Key Modules

### 4.1 Speech Module
- Uses Indic-ASR for Indian languages.
- Supports:
  - Hindi
  - Telugu
  - Tamil
  - Kannada
  - Marathi
  - English

### 4.2 NLP & Intent Module
- Identifies whether user is asking about:
  - Eligibility
  - Documents
  - Application steps
  - Scheme details

### 4.3 Scheme Information Module
- Structured JSON database containing:
  - Scheme name
  - Description
  - Eligibility
  - Documents
  - Steps to apply

### 4.4 Text-to-Speech Module
- Converts AI responses into audio using gTTS or Festival TTS.

---

## 5. Technology Stack

### Frontend
- React + Vite
- Tailwind CSS
- Web Speech API (where supported)

### Backend
- FastAPI (Python)

### AI & Language
- Indic-ASR (Speech-to-Text)
- Open-source LLM (Llama/IndicBERT)
- gTTS / Festival TTS

### Database
- SQLite or Firebase (Free Tier)

### Cloud
- AWS EC2 (Backend)
- AWS S3 + CloudFront (Frontend)

---

## 6. Security & Privacy

- No storage of sensitive personal data.
- Minimal data collection.
- Secure HTTPS communication.
- No tracking or user profiling.

---

## 7. Scalability & Future Scope

Future enhancements include:
- More Indian languages.
- More government schemes.
- Mobile app version.
- Offline mode.
- Panchayat dashboard integration.

---

## 8. Assumptions

- Internet connectivity is available (even if slow).
- Users access via mobile or desktop browser.
- Open-source AI tools are sufficient for multilingual support.

---

## 9. Conclusion

This design ensures that AI Bharat Sahayak is:
- Accessible
- Inclusive
- Scalable
- Cost-effective
- Aligned with the “AI for Bharat” vision.
