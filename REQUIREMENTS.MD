

## 1. Project Overview
AI Bharat Sahayak is a free, multilingual, web-based AI assistant that helps Indian citizens understand and access government schemes through simple conversation in their own language. The system supports both voice and text input and provides clear, step-by-step guidance on scheme eligibility, documents, and application processes.

## 2. Problem Statement
Many citizens in India face difficulties in understanding government schemes due to:
- Language barriers
- Complex bureaucratic terminology
- Lack of digital literacy
- Scattered information across multiple websites

This leads to low awareness and poor adoption of welfare benefits.

## 3. Objectives
The system aims to:
- Provide a single platform for government scheme information
- Support multiple Indian languages
- Enable voice-based interaction for low-literacy users
- Simplify complex scheme details into plain language
- Reduce dependency on middlemen and agents

## 4. Functional Requirements

### 4.1 User Interaction
The system must:
- Accept voice input in Hindi, Telugu, Tamil, Kannada, Marathi, and English
- Accept text input in the same languages
- Convert speech to text using open-source ASR
- Understand user intent using an AI model
- Provide responses in the user's selected language
- Convert text responses into speech output

### 4.2 Scheme Information Module
The system should:
- Store details of major government schemes such as:
  - Ayushman Bharat
  - PMAY (Pradhan Mantri Awas Yojana)
  - Ration Card
  - Old Age Pension
- Provide:
  - Scheme description
  - Eligibility criteria
  - Required documents
  - Step-by-step application process
  - Online/offline application links or locations

### 4.3 Eligibility Checker
The system must:
- Ask simple yes/no questions to assess eligibility
- Provide a clear eligibility result
- Suggest next steps if eligible

### 4.4 Accessibility
The system should:
- Work on basic smartphones and low-end devices
- Function on low-bandwidth internet
- Not require user login or registration
- Be completely free to use

## 5. Non-Functional Requirements

### 5.1 Performance
- Response time should be under 5 seconds for most queries
- System should handle multiple users simultaneously

### 5.2 Security & Privacy
- No storage of sensitive personal data
- Secure communication between frontend and backend
- Minimal data collection

### 5.3 Scalability
- System should be deployable on AWS Free Tier
- Should support future addition of more languages and schemes

### 5.4 Usability
- Simple and intuitive UI
- Clear buttons for mic and text input
- Easy language selection dropdown

## 6. Constraints
- Must use only free or open-source tools
- No paid APIs or subscriptions allowed
- Must be deployable on AWS Free Tier

## 7. Deliverables
The team will submit:
- requirements.md (this file)
- design.md generated via Kiro
- GitHub repository link
- Presentation in PDF format using official template

## 8. Success Criteria
The project will be considered successful if:
- Users can ask questions in their language
- System provides correct and simple answers
- Voice input and output work properly
- Website runs smoothly on basic devices
- All hackathon submission requirements are met
