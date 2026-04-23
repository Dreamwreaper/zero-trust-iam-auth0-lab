# Zero Trust IAM Demo (Auth0 + Node.js)

End-to-end Identity & Access Management lab demonstrating authentication, authorization, and MFA enforcement using Auth0 and a Node.js (Express) app.

## 🔐 What This Demonstrates
- **OIDC Authentication** via Auth0
- **Federated Login** (Google) vs **Local DB Login**
- **OAuth Consent Flow** (user grants scopes)
- **Session Management** with Express + Passport
- **MFA (TOTP) Enrollment & Enforcement**
- **Policy-Based Access Control** (MFA = Always)

## 🏗️ Architecture
- **IdP**: Auth0
- **App**: Node.js (Express)
- **Auth**: Passport + `passport-auth0`
- **Session**: `express-session`
- **MFA**: TOTP via Authenticator apps

## ⚙️ Setup
```bash
git clone <your-repo>
cd zero-trust-auth
npm install
