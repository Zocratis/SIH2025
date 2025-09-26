# Fake Certificate Detection & Authentication Platform

## 🏆 Problem Statement
With increasing digitization, the problem of fake degrees and forged academic certificates has become a major concern for higher education institutions, employers, and government bodies. Verification today is often manual and inconsistent, leading to corruption and misuse.

Our solution aims to create a **smart, secure, and scalable digital platform** for detecting and authenticating academic certificates across Jharkhand.

---

## 🎯 Objectives
- Detect and prevent the use of **fake or tampered degrees/certificates**.
- Support **both legacy (scanned)** and **new (ERP-issued)** certificates.
- Enable **employers, universities, and government departments** to easily verify certificates.
- Provide an **admin dashboard** for forgery monitoring and blacklisting offenders.
- Future-proof the system with **blockchain integration**.

---

## 🔑 Key Features
1. **Employer Verification Portal**
   - Upload a certificate (PDF/JPEG).
   - OCR extraction + database + blockchain hash verification.
   - Confidence score and explainable reasons for results.

2. **Institution Integration Module**
   - Universities/colleges can bulk-upload records (CSV) or real-time upload via ERP.
   - Certificates are hashed (SHA-256) and optionally anchored on blockchain.

3. **Admin Dashboard**
   - Monitor verification activity.
   - Detect forgery trends with graph-based analysis.
   - Manage blacklisted institutions or offenders.

4. **AI-powered Detection**
   - OCR + NLP validation for course/institution names.
   - Siamese CNN for signature/seal matching.
   - Autoencoder/One-Class SVM for anomaly detection in legacy scanned certificates.

5. **Blockchain Simulation**
   - Prevents fake entries in the future by hashing new certificates.
   - Prototype uses simulated blockchain; future scope includes Polygon/Hyperledger.

---

## 🏗️ System Architecture
![Architecture Diagram](architecture-diagram.png)

- **Frontend**: React + Tailwind
- **Backend**: Node.js (Express + Sequelize + PostgreSQL)
- **OCR Service**: FastAPI + Tesseract
- **ML Service**: FastAPI + PyTorch/Scikit-learn
- **Blockchain (Sim)**: SHA-256 Hashing + mock txHash

---

## ⚡ Workflow
1. Employer uploads certificate.
2. OCR extracts key details (Name, Roll No, Course, Marks, Cert ID).
3. Backend matches against institutional records.
4. Blockchain registry verifies hash (for ERP-issued certs).
5. ML models check signatures, seals, anomalies.
6. Result returned with **confidence score + explainable reasons**.
7. Logs stored in DB; suspicious cases flagged for admin review.

![Workflow Diagram](workflow-diagram.png)

---

## 📂 Project Structure

---

## 🛠️ Tech Stack
- **Frontend**: React, Tailwind, Recharts, Framer Motion
- **Backend**: Node.js, Express, Sequelize, PostgreSQL
- **OCR**: Tesseract, OpenCV, FastAPI
- **ML Models**: PyTorch, Scikit-learn, HuggingFace Transformers
- **Blockchain**: SHA-256 simulation (future: Polygon/Hyperledger)
- **Other Tools**: Faker (dataset gen), Docker (optional), NetworkX (graph forensics)

---

## 📊 Differentiators
Unlike plain OCR + CNN solutions, our project adds:
- Blockchain-backed prevention (not just detection).
- Graph-based forgery pattern analysis (network-level detection).
- NLP validation of institution/course names.
- Explainable AI (results show reasons, not just “fake/genuine”).
- Privacy-preserving design (hash-based verification).

---

## 🚀 Future Scope
- Full blockchain deployment (Polygon/Hyperledger).
- Direct integration with **DigiLocker APIs**.
- Advanced anomaly detection using Vision Transformers.
- Zero-Knowledge Proofs for privacy-preserving verification.
- Nationwide rollout for **all Indian universities**.

---

## 👥 Team
- [CODEMONKS] — [MUKESHPATELINSTITUTEOFTECHNOLOGYMANAGEMENT]  
- Members: [JayBharatia], [DeepanshuBansal], [VandanChoksi], [MansiBharambe],[ArnavJhadav],[VaedantAgarwal]
- Mentors: [Mentor Name]  

---

## 📌 References
- [GPDS Handwritten Signature Dataset](http://www.gpds.ulpgc.es/)
- [Tesseract OCR](https://github.com/tesseract-ocr/tesseract)
- [DigiLocker](https://www.digilocker.gov.in/)
- UGC & Jharkhand State Universities List
