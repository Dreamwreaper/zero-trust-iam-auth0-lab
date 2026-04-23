# 🔐 Zero Trust IAM Lab (Auth0 + Node.js)

End-to-end Identity & Access Management (IAM) project demonstrating authentication, authorization, and enforced multi-factor authentication (MFA) using Auth0 and a Node.js (Express) application.

---

## 🚀 Overview

This project simulates a real-world IAM implementation, including:

- OpenID Connect (OIDC) authentication  
- OAuth 2.0 authorization + consent flow  
- Federated identity (Google)  
- Local identity (database-backed users)  
- MFA enforcement using TOTP (Authenticator apps)  
- Session-based access control  

---

## 🏗️ Architecture

- **Identity Provider (IdP):** Auth0  
- **Application:** Node.js (Express)  
- **Authentication:** Passport.js + passport-auth0  
- **Session Management:** express-session  
- **MFA:** Time-based One-Time Password (TOTP)  

---

## 🔐 Authentication Flows

### Federated Login (Google)
- User authenticates via Google  
- Auth0 trusts external IdP  
- OAuth consent screen displayed  
- Redirect to application dashboard  

### Database Login (Local Users)
- Username/password authentication via Auth0 database  
- Controlled by internal identity store  
- MFA enforced via policy  

---

## 🛡️ MFA Implementation

- Enabled One-Time Password (OTP) factor  
- Configured policy: Always Require MFA  
- Enforced for all database users  

Users complete:
- QR Code enrollment  
- 6-digit TOTP verification  

---

## ⚙️ Setup Instructions

### Clone Repository
git clone https://github.com/YOUR_USERNAME/zero-trust-iam-auth0-lab.git  
cd zero-trust-iam-auth0-lab  

### Install Dependencies
npm install  

### Configure Environment Variables

Create a `.env` file in the root directory:

AUTH0_DOMAIN=your-tenant.us.auth0.com  
AUTH0_CLIENT_ID=your-client-id  
AUTH0_CLIENT_SECRET=your-client-secret  
AUTH0_CALLBACK_URL=http://localhost:3000/callback  
SESSION_SECRET=supersecret  

### Run Application
node app.js  

### Access the Application
http://localhost:3000  

---

## 📸 Suggested Screenshots (for portfolio impact)

Add these to a `/screenshots` folder:

- Auth0 Dashboard (Application configured)  
- Database Connection enabled  
- User creation screen  
- Login page (Auth0 Universal Login)  
- MFA QR code enrollment  
- Successful login dashboard  

---

## 🧠 Key IAM Concepts Demonstrated

- Identity Federation vs Local Authentication  
- OAuth 2.0 Authorization Flow  
- OpenID Connect (OIDC) Authentication  
- MFA Enforcement (TOTP)  
- Session Management & Protected Routes  
- Zero Trust Authentication Principles  

---

## 🔐 Security Considerations

- Secrets stored in `.env` (not committed to repo)  
- MFA enforced via policy (not optional)  
- Separation of identity providers (federated vs local)  
- Protected routes require authentication  

---

## 💼 Real-World Relevance

This project aligns with:

- Zero Trust Architecture principles  
- NIST SP 800-53 (IA-2, AC-2, AC-7)  
- Enterprise IAM platforms (Auth0, Okta, Entra ID)  

---

## 🗣️ Interview Summary

Built a Zero Trust IAM lab using Auth0 and Node.js implementing OIDC authentication, OAuth authorization, and enforced TOTP-based MFA. Demonstrated federated and local identity flows with policy-based access control.

---

## 📄 License
MIT
