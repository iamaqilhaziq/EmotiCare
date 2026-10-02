# EmotiCare System Architecture

## Overview

EmotiCare uses a modular web-based architecture that integrates the user-facing web application, relational database, and AI-assisted emotional analysis service.

The architecture supports emotional assessments, mood monitoring, digital journaling, wellness activities, emotional results, administrative management, and AI-assisted emotional analysis within a unified platform.

---

## High-Level Architecture

```text
                    ┌─────────────────────┐
                    │        User         │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │     Web Browser     │
                    └──────────┬──────────┘
                               │
                               ▼
                  ┌─────────────────────────┐
                  │ EmotiCare Web Platform │
                  └────────────┬────────────┘
                               │
                  ┌────────────┴────────────┐
                  │                         │
                  ▼                         ▼
        ┌─────────────────┐       ┌─────────────────┐
        │ MySQL Database  │       │ Python AI       │
        │                 │       │ Service         │
        └─────────────────┘       └─────────────────┘
```

---

## 1. User Layer

Users access EmotiCare through a standard web browser.

The platform supports different types of users, including:

- Students
- Staff
- Organisational users
- Administrators

The responsive web interface allows the platform to be accessed using desktop, tablet, and mobile devices.

---

## 2. Web Application Layer

The main EmotiCare web application is developed using:

- PHP
- HTML
- CSS
- JavaScript

The web application layer manages interaction between users, application functions, the database, and supporting services.

Major functions include:

- User authentication
- Emotional assessments
- Mood check-ins
- Digital journaling
- Wellness activities
- Mind games
- Assessment results
- Emotional progress monitoring
- Support mechanisms

---

## 3. Database Layer

MySQL is used as the relational database management system for EmotiCare.

The database supports information related to:

- User accounts
- Assessment questions
- Assessment answers
- Assessment results
- Mood records
- Journal records
- Activities
- Counsellors
- Authentication information
- System activity records

Sensitive database structures, credentials, production data, and configuration details are intentionally excluded from this repository.

---

## 4. AI Service Layer

EmotiCare incorporates a Python-based AI service using Flask.

The AI service supports journal emotional analysis through processes including:

- Sentiment analysis
- Text feature extraction
- Emotion classification
- Intervention determination

The current emotional analysis approach incorporates:

- VADER
- TF-IDF
- Logistic Regression

The AI service communicates with the EmotiCare web application as part of the emotional analysis workflow.

---

## 5. Authentication and Access Layer

EmotiCare incorporates authentication and access-control mechanisms to protect platform functions and user information.

These mechanisms include:

- User authentication
- Account verification
- Account status controls
- Login attempt controls
- Session management
- Session timeout
- Role-based access
- Passkey / WebAuthn support

Detailed security configurations and production implementation are intentionally not disclosed.

---

## 6. User Interaction Flow

A general user interaction with the platform follows this process:

```text
User
  │
  ▼
Web Browser
  │
  ▼
EmotiCare Web Platform
  │
  ├──────────────► MySQL Database
  │
  └──────────────► AI Service
                       │
                       ▼
                Emotional Analysis
                       │
                       ▼
                Analysis Result
                       │
                       ▼
                EmotiCare Platform
                       │
                       ▼
                      User
```

---

## 7. Modular Design

EmotiCare separates major platform functions into different functional components.

This approach supports:

- Maintainability
- Separation of system functions
- Integration of AI-assisted services
- Future platform development
- Expansion of emotional-care capabilities

---

## Architecture Principle

The EmotiCare architecture is designed around a human-centered digital care approach.

Technology is used to support emotional self-awareness, monitoring, and access to appropriate support while maintaining the role of human support where required.

---

> **Note:** This document presents a high-level system architecture. Production source code, database credentials, API credentials, server configurations, and security-sensitive implementation details are not included.