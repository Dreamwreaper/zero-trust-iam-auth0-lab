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
- **Authentication:** Passport.js + `passport-auth0`  
- **Session Management:** `express-session`  
- **MFA:** Time-based One-Time Password (TOTP)  

---

## 🔐 Authentication Flows

### 1. Federated Login (Google)
- User authenticates via Google  
- Auth0 trusts external IdP  
- OAuth consent screen displayed  
- Redirect to application dashboard  

### 2. Database Login (Local Users)
- Username/password authentication via Auth0 database  
- Controlled by internal identity store  
- MFA enforced via policy  

---

## 🛡️ MFA Implementation

- Enabled **One-Time Password (OTP)** factor  
- Configured policy: **Always Require MFA**  
- Enforced for all database users  

Users complete:
- QR Code enrollment  
- 6-digit TOTP verification  

---

## ⚙️ Setup Instructions

### 1. Clone Repo
```bash
git clone https://github.com/YOUR_USERNAME/zero-trust-iam-auth0-lab.git
cd zero-trust-iam-auth0-lab
2. Install Dependencies
npm install
3. Configure Environment Variables

Create a .env file:

AUTH0_DOMAIN=your-tenant.us.auth0.com
AUTH0_CLIENT_ID=your-client-id
AUTH0_CLIENT_SECRET=your-client-secret
AUTH0_CALLBACK_URL=http://localhost:3000/callback
SESSION_SECRET=supersecret
4. Run Application
node app.js
5. Access the App
http://localhost:3000
