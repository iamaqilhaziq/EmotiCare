# EmotiCare Technology Stack

## Overview

EmotiCare combines web development technologies, database technologies, AI-assisted text analysis, and authentication mechanisms to provide an integrated emotional and mental health support platform.

This document provides a high-level overview of the technologies used without exposing production implementation details.

---

## Technology Summary

| Component | Technology |
|---|---|
| Backend | PHP |
| Frontend | HTML, CSS, JavaScript |
| Database | MySQL |
| AI Service | Python, Flask |
| Sentiment Analysis | VADER |
| Text Feature Extraction | TF-IDF |
| Emotion Classification | Logistic Regression |
| Authentication | Session Authentication |
| Passwordless Authentication | Passkey / WebAuthn |

---

## 1. Backend

### PHP

PHP is used as the primary server-side technology for the EmotiCare web application.

The backend supports functions such as:

- User authentication
- User account management
- Assessment processing
- Mood management
- Journal management
- Activity management
- Result management
- Database interaction
- Integration with supporting services

---

## 2. Frontend

The EmotiCare user interface is developed using standard web technologies.

### HTML

HTML provides the structural foundation of the web interface.

### CSS

CSS is used for:

- Interface styling
- Layout
- Responsive presentation
- Visual consistency
- Component presentation

### JavaScript

JavaScript supports interactive behaviour within the web application.

It is used to enhance user interaction and dynamic interface functionality.

---

## 3. Database

### MySQL

MySQL is used as the relational database management system.

The database supports structured platform information including:

- Users
- Assessments
- Answers
- Results
- Mood records
- Journal records
- Activities
- Counsellors
- Authentication information
- System activity information

Production database schemas, credentials, and sensitive records are not included in this repository.

---

## 4. AI Service

### Python

Python is used for AI-assisted emotional text analysis.

### Flask

Flask provides the service layer used to connect AI-assisted analysis with the EmotiCare web application.

The AI service processes relevant text information and returns analysis results to the web application.

---

## 5. Sentiment Analysis

### VADER

VADER is incorporated into the journal emotional analysis workflow to obtain sentiment information from text.

Sentiment information contributes to the broader emotional analysis process.

---

## 6. Text Feature Extraction

### TF-IDF

TF-IDF is used to transform textual information into numerical features.

These features can then be processed by the emotion classification model.

---

## 7. Emotion Classification

### Logistic Regression

Logistic Regression is used as part of the current emotion classification workflow.

---

## 8. Authentication

EmotiCare incorporates multiple mechanisms for user authentication and access protection.

These include:

- User credentials
- Account verification
- Login attempt controls
- Session management
- Session timeout
- Role-based access

---

## 9. Passkey / WebAuthn

EmotiCare supports Passkey / WebAuthn as an additional authentication capability.

This provides an alternative authentication mechanism supported by modern web technologies.

Detailed cryptographic implementation and production configuration are intentionally excluded.

---

## 10. Technology Integration

The major technologies interact at a high level as follows:

```text
HTML / CSS / JavaScript
          │
          ▼
         PHP
       ┌──┴──┐
       │     │
       ▼     ▼
     MySQL  Python / Flask
               │
               ▼
       Emotional Analysis
       ┌───────┼───────────┐
       ▼       ▼           ▼
     VADER   TF-IDF   Logistic Regression
```

---

## Technology Design Principle

The technology stack separates major responsibilities between:

- User interface
- Web application logic
- Data management
- AI-assisted analysis
- Authentication and access protection

This modular approach supports the continued development and integration of EmotiCare functionality.

---

> **Note:** Production source code, credentials, API configurations, database configurations, cryptographic details, and server configurations are intentionally excluded from this repository.