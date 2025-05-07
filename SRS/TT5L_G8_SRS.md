# Software Requirements Specification (SRS)

## 1. Introduction

### 1.1 Purpose - adriana
The purpose of the Student Club Management System with Budget and Venue Integration is to provide a unified digital platform that streamlines the administrative and operational tasks of student clubs and organizations within the university. The system is developed to address the inefficients of current club workflows, which are often handled through disconnected tools like email, spreadsheets, and standalone forms. These manual processes lead to miscommunication, lost records, and delays in approvals. By integrating with the university's financial management system and campus venue reservation database, the platform will centralize core operations such as membership management, event planning, budget tracking, and venue booking. The system will support role-based access for student club leaders, members, finance officers, faculty advisors, and space managers, enabling them to perform and approve actions within their responsibilities. This will ensure faster workflows, clear accountability, and better compliance with university regulations. Ultimately, the platform aims to enhance the student co-curricular experience by making club operations more efficient, transparent, and accessible across all levels of involvement.

### 1.2 Scope - rafida
*Define the scope of the system, what it will and will not do.*

### 1.3 Product Overview

#### 1.3.1 Product Perspective - sofea
*Explain how this product fits within existing systems or projects.*

#### 1.3.2 Product Functions - amirah
*List the key features or use cases the system will support.*

#### 1.3.3 User Characteristics - adriana
The primary users of the Student Club Management System with Budget and Venue Integration include student club leaders such as presidents, secretaries, and treasurers, as well as regular club members, faculty advisors, finance officers, and space managers. Student users are expected to have basic digital skills, commonly using tools like email, Google Forms, and social media to manage or interact with clubs. They are typically undergraduate students and may not have technical experience beyond general productivity software. Club leaders, while also students, are expected to handle more administrative features of the system, including member databases, event planning, and proposal submissions. Faculty advisors serve in a supervisory role and are assumed to have basic familiarity with approval workflows and club activity monitoring. Finance officers and space managers, who are part of the university's administrative departments, are expected to have moderate to high proficiency with institutional systems, particularly for reviewing and processing budget proposals and venue bookings. The system interface will be designed with a clean, intuitive layout to accomodate all user types, minimizing the learning curve and reducing the need for training. Accessibility features and responsive design will be prioritized to ensure usability across different devices and user needs.

#### 1.3.4 Limitations - rafida
*Mention any constraints such as hardware, software, or regulations.*

### 1.4 Definitions - sofea
*Define all technical terms, acronyms, or jargon used in the document.*

---

## 2. References - everyone

CampusGroups. (2024). *CampusGroups – Student engagement and event management platform*. https://www.campusgroups.com

ClubExpress. (2024). *ClubExpress – Club and association management*. https://www.clubexpress.com

Hello Club. (2024). *Hello Club – Membership management software*. https://www.helloclub.com

IEEE. (2018). *ISO/IEC/IEEE 29148:2018 Systems and software engineering—Life cycle processes—Requirements engineering*. International Organization for Standardization. https://www.iso.org/standard/72089.html

Pohl, K. (2010). *Requirements engineering: Fundamentals, principles, and techniques*. Springer.

Pressman, R. S., & Maxim, B. R. (2015). *Software engineering: A practitioner’s approach* (8th ed.). McGraw-Hill Education.

Sommerville, I. (2016). *Software engineering* (10th ed.). Pearson Education.

---

## 3. Requirements

### 3.1 Functions - amirah
*Detail all functional requirements of the system.*

### 3.2 Performance Requirements - adriana
The system shall be capable of handling concurrent access from at least 500 active users during peak registration and event planning periods without performance degradation. Page load times shall not exceed 2 seconds under normal load conditions, and transaction responses, such as budget submission and venue request must be processed within 3 seconds at a minimum throughput of 100 transactions per minute. The system shall maintain an uptime of 99.5% monthly, with scheduled maintenance periods announced in advance. For database operations, queries related to event schedules, budget approvals, and club listings must execute in under 1.5 seconds. The system shall support scalability to allow future integration with mobile platforms or additional student service modules. Latency-sensitive features, such as real-time venue availability checking, must provide results with less than 1 second delay to ensure responsive interaction during booking. In addition, backup operations shall be automated and completed within 15 minutes daily to avoid data loss in case of failure.

### 3.3 Usability Requirements - rafida
*Specify requirements for ease of use, accessibility, or user training.*

### 3.4 Interface Requirements - sofea
*Describe user interfaces, APIs, hardware interfaces, etc.*

### 3.5 Logical Database Requirements - amirah
*Detail any data storage needs, database schema, and relationships.*

### 3.6 Design Constraints - adriana
The Student Club Management System must be developed as a web-based application compatible with all major browsers including Chrome, Firefox, Safari, and Microsoft Edge, ensuring accessibility accross different operating systems. It must adhere to the university's branding guidelines and integrate with existing financial management and campus scheduling systems via RESTful APIs. The system must be implemented using open-source technologies to reduce licensing costs, with a preferred technology stack including Node.js, React, and PostgreSQL. The software must also comply with the university's data security and privacy policies, including secure login, encrypted communication (SSL/TLS), and role-based access control (RBAC). Hosting shall be on the university's private cloud or an approved public cloud provider that meets the Malaysian Personal Data Protection Act(PDPA) compliance. Furthermore, the system interface must follow Web Content Accessibility Guidelines (WCAG) 2.1 to support users with disabilities, and all third-party libraries used must be well-documented and actively maintained.

### 3.7 Software System Attributes - rafida
*Discuss system qualities like reliability, maintainability, security.*

### 3.8 Supporting Information - sofea
*Include mockups, diagrams, additional documentation if needed.*

---

## 4. Verification
*Describe how each requirement in Section 3 will be verified (testing, demo, review, etc.). Match section numbers.*

### 4.1 Functional Requirements - amirah
*Detail all functional requirements of the system.*

### 4.2 Performance Requirements - adriana
How: Performance verification will be conducted using automated performance testing tools such as JMeter and LoadRunner to stimulate high user concurrency, data loads, and transaction volumes.
Who: The testing team in collaboration with university IT support staff will carry out the verification.
When: Testing will be executed after system integration is complete and before full deployment, specifically during the UAT (User Acceptance Testing) phase.
Where: Performance tests will be run in a staging environment that mirrors the production setup.
Criteria: The system must pass the defined benchmarks including: (1) page load time not exceeding 2 seconds, (2) 500 concurrent users without performance drop, (3) venue query response time within 1 second, and (4) daily backup operation successfully completed in under 15 minutes. Any failure to meet these benchmarks will require refactoring and retesting.

### 4.3 Usability Requirements - rafida
*Specify requirements for ease of use, accessibility, or user training.*

### 4.4 Interface Requirements - sofea
*Describe user interfaces, APIs, hardware interfaces, etc.*

### 4.5 Logical Database Requirements - amirah
*Detail any data storage needs, database schema, and relationships.*

---

## 5. Appendices

### 5.1 Assumptions and Dependencies - everyone
This system assumes that student clubs are registered through a centralized university database and that each club has designated officers with authority to request budgets and book venues. It depends on stable integration with the university's financial management system, such as for fund tracking and approvals, and the venue booking database, such as for real-time availability and scheduling. It also assumes continuous availability of authentication services provided by the university's Single Sign-On (SSO) system. Internet access is assumed for both students and staff. Additionally, administrative users are expected to respond to requests within designated processing time frames. The system also assumes that all policy changes, such as new budget rules or booking protocols, will be updated in the admin panel by authorized university staff. Lastly, the development team depends on timely access to relevant documentation, data, and technical support from the university's IT department during both development and maintenance phases.

### 5.2 Acronyms and Abbreviations - everyone
API - Application Programming Interface
DBMS - Database Management System
GUI - Graphical User Interface
HTTP - HyperText Transfer Protocol
PDPA - Personal Data Protection Act
RBAC - Role-Based Access Control
SRS - Software Requirement Specification
SSL - Secure Sockets Layer
SSO - Single Sign-On
UAT - User Acceptance Testing
WCAG - Web Content Accessibility Guidelines

