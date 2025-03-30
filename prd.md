**Product Requirements Document (PRD) for Booie Education Platform**

---

### 1. Overview

**Project Name:** Booie Education Platform  
**Goal:** Build a functional MVP with a fully operational front end and back end to attract potential investors and bank partners.  
**Target Users:** Students seeking educational loans

---

### 2. Objectives

- Seamless front-end experience for students
- Robust back-end architecture for secure and reliable data handling
- Full compliance with US student lending and data protection regulations

---

### 3. Front-End Requirements

#### 3.1 Features
- **Income Trajectory Projection:** Based on school and degree program, provide a visual projection of income over time (displayed in annualized terms).
- **Loan Calculator:** Real-time, interactive calculator with inputs for loan amount, interest rate, and repayment period. Limits imposed to prevent predatory terms.
  - **Back-End Logic:** Repayment rate is derived from the algorithm targeting a 0% excess IRR (cell E20 in the financial model). In production, this should be implemented via a loop in Python mimicking Excel’s Solver add-in.
  - **Monthly Calculation:** Internal logic should be calculated monthly, with user-facing outputs presented annually (salary projections) and monthly (repayments).
- **Loan Comparison Tool:** Easily interpretable comparison between Booie plans and other common lending options.
- **Fee Structure Page:** Detailed, user-friendly explanation of Booie’s fee structure compared to alternatives.
- **FAQ Page:** Commonly asked questions and clear, concise answers.
- **Contact Page:** Basic contact form or customer service chatbot.
- **Secure Account Management:** Sign-up/login flows with password hashing and optional 2FA.
- **Loan Application Form:** Auto-pre-approval based on loan algorithm. Include secure document upload for verification.

#### 3.2 Front-End Regulatory Compliance
- **TILA:** Clear finance charges and APR disclosures.
- **AML/KYC:** Identity verification integration (e.g., ID upload + selfie match).
- **ECOA:** Ensure approval algorithms are fair and unbiased.
- **GLB Act Privacy Rule:** Clear, prominent privacy policy hyperlink and consent checkbox.
- **Dodd-Frank/UDAAP:** Transparent communication and fee disclosures.
- **Student Borrower Rights:** Display comparison of Booie and federal loan options.

**Note:** Most front-end regulatory requirements are static disclosures and linked documents. Ensure they are clearly accessible from relevant transaction pages.

---

### 4. Back-End Requirements

#### 4.1 Architecture Principles
- **Reliability:** Ensure uptime, integrity of incoming and outgoing data.
- **Security:** Implement data encryption, secure API access, and audit logs.
- **Governance:** Full documentation for partner due diligence.
- **Modularity:** Microservice architecture to allow scalable, flexible data handling.

#### 4.2 Features
- Secure database and file storage (e.g., AWS RDS + S3)
- Internal API for calculator, approval algorithm, and data ingestion
- Admin dashboard with exportable reports (CSV, PDF)
- Pre-built analytics dashboards (loan funnel, approval rates, revenue modeling)
- Access control system for internal staff roles
- Optional: Integrate with SaaS tools for security and logging

#### 4.3 Back-End Regulatory Compliance
- **GLB Act Safeguards Rule:**
  - Role-based access control (RBAC)
  - Full data inventory and encryption (in transit and at rest)
  - Multi-factor authentication (MFA)
  - Security change management plan
  - Access logs + intrusion detection
  - Onboarding and incident response documentation
  - Flagging suspicious logins and unauthorized access attempts

**Note:** Back-end security is paramount. Many controls (e.g., logging, MFA, suspicious activity detection) may be managed using SaaS compliance/security solutions.

---

### 5. Technical Stack (Suggested)

| Layer        | Tool/Framework                |
|--------------|-------------------------------|
| Front End    | React, Next.js, Tailwind CSS  |
| Back End     | Node.js, Express.js           |
| Database     | PostgreSQL                    |
| Storage      | AWS S3                        |
| Authentication | Auth0 / Firebase Auth     |
| Deployment   | Vercel (front end), AWS (back end) |

---

### 6. Milestones

| Milestone                        | ETA          |
|----------------------------------|--------------|
| Wireframes and UI Design         | Week 1       |
| Front-End MVP                    | Week 3       |
| Back-End MVP                     | Week 4       |
| Compliance Features              | Week 5       |
| Internal QA + Feedback Iteration| Week 6       |
| MVP Launch                       | Week 7       |

---

### 7. Notes
- Connect with legal advisor to ensure compliance language is up to date.
- Coordinate closely between design and backend teams to validate form logic and data model.
- Keep investor reporting formats in mind when building database schema.
- Refer to loan calculator algorithm and Excel financial model for loan repayment logic implementation.
- Existing back-end flow diagrams may not be fully applicable (e.g., mobile app not currently required).

---

**End of PRD**

