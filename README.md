# 🏠 Roommate Matching System
### System Analysis & Design — Full Architectural Specification

> **Grade: A** | Don State Technical University | B.Sc. Information Technology | 2024–2025

---

## Overview

A comprehensive system analysis and design project for a preference-based roommate 
compatibility and student housing platform. This repository contains the full 
architectural specification — from requirements engineering through to REST API design.

The system eliminates reliance on informal communication by providing structured 
compatibility matching, controlled student communication, roommate group formation, 
and joint housing application processing.

---

## Problem Statement

Modern universities face growing pressure to digitise housing processes. 
Roommate matching involves several interdependent concerns:
- Compatibility assessment — matching students by preferences and lifestyle
- Connection request handling — managing invitation and acceptance flows
- Group formation — coordinating multi-student housing groups
- Agreement confirmation — ensuring all parties consent before submission
- Joint housing application — submitting a single coordinated application

---

## Stakeholders

| Stakeholder | Role |
|---|---|
| **Students** | Create profiles, define preferences, browse matches, message, form groups, submit applications |
| **Housing Administrators** | Review submitted applications, record approval/rejection decisions |
| **Authentication Provider** | University credential verification (SSO) |
| **Notification Service** | Automated alerts for requests, invitations, and decisions |

---

## Design Artefacts

Six complementary modelling notations were applied:

| Artefact | Notation | Purpose |
|---|---|---|
| Business Process Models | BPMN 2.0 | End-to-end process flows |
| Data Flow Diagrams | Yourdon-DeMarco | Data movement through system |
| ER Diagram + Data Dictionary | Standard relational | Database structure |
| Class Diagram | UML 2.5 | Object structure and relationships |
| Sequence Diagrams | UML 2.5 | Component interaction flows |
| State Diagram | UML 2.5 | Application lifecycle states |

---

## System Architecture

- **Style:** Layered microservices-adjacent architecture
- **Authentication:** University SSO + JWT
- **Database Strategy:** Relational database with preference-vector matching
- **Deployment:** Cloud-deployable with independent service scaling

---

## Sample API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| `POST` | `/auth/login` | University credential authentication |
| `GET` | `/students/matches` | Compatibility-ranked match results |
| `POST` | `/connections/request` | Send roommate connection request |
| `PUT` | `/connections/{id}/accept` | Accept pending connection |
| `POST` | `/groups` | Create roommate group |
| `POST` | `/applications` | Submit joint housing application |
| `PUT` | `/applications/{id}/decision` | Admin: record decision |

---

## Repository Structure
roommate-matching-system/
├── docs/
│   ├── coursework-report.pdf     ← Upload your actual document here
│   ├── diagrams/
│   │   ├── use-case-diagram.png
│   │   ├── bpmn-diagrams/
│   │   ├── er-diagram.png
│   │   ├── class-diagram.png
│   │   ├── sequence-diagrams/
│   │   └── state-diagram.png
│   └── api-specification.md
└── README.md
---

## Key Design Decisions

**Preference-based matching** — compatibility scores computed from weighted preference 
vectors (sleep schedule, study habits, cleanliness, social preferences).

**Controlled communication** — messaging restricted to mutually connected students 
for safety and moderation.

**Group consensus** — all members must individually confirm before joint application 
submission, preventing coercion or premature submission.

---

## Author

**Umar Hamza Maishanu**  
B.Sc. Information Technology, DSTU Russia  
[LinkedIn](https://linkedin.com/in/umarhamzamaishanu) · [GitHub](https://github.com/UmarMaishanu)

---
*System analysis and architectural design artefact — specification phase of software development.*
