# backend-guidelines.md

## API
- Use REST or GraphQL (depending on team preference)
- Secure all endpoints (JWT-based auth preferred)

## Core Services
- Repayment rate algorithm (IRR = investor return)
- KYC/AML integration
- Auto-pre-approval system

## Data Security
- Encrypt data at rest (AES-256) and in transit (TLS)
- Log all access, flag suspicious logins
- Use SaaS solutions for logging/security if possible

## Architecture
- Modular services for scaling
- Follow 12-factor app principles
