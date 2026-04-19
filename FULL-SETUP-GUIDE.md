# Full Setup Guide for Independence Services NZ Coder

## Table of Contents
1. [Backend API Files](#backend-api-files)
2. [Email Setup](#email-setup)
3. [Admin Dashboard](#admin-dashboard)
4. [Vercel Deployment](#vercel-deployment)
5. [Testing](#testing)

---

## Backend API Files

### Prerequisites
- Node.js and npm installed
- MongoDB server (or any other database) running

### Setup Steps
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/independenceservicesnz-coder/independenceservicesnz-coder.github.io.git
   cd independenceservicesnz-coder.github.io/backend
   ```
2. **Install Dependencies**:
   ```bash
   npm install
   ```
3. **Configure Environment Variables**:
   Create a `.env` file based on `.env.example` with relevant fields set up (DB connection string, API keys, etc.).
4. **Migrate Database** (if applicable):
   ```bash
   npm run migrate
   ```
5. **Start the API**:
   ```bash
   npm start
   ```

## Email Setup

### Prerequisites
- An email provider (like SendGrid, Mailgun, etc.)

### Setup Steps
1. **Install Email Provider SDK**:
   ```bash
   npm install <provider-sdk>
   ```
2. **Configure Email Service**:
   Update the `.env` file with email provider credentials.
3. **Implement Email Logic**:
   Use the SDK to send emails (see [provider documentation](#)).
   ```javascript
   const emailService = require('<provider-sdk>');
   emailService.send({ ... });
   ```

## Admin Dashboard

### Prerequisites
- React or any other frontend framework

### Setup Steps
1. **Navigate to Dashboard Directory**:
   ```bash
   cd ./dashboard
   ```
2. **Install Dependencies**:
   ```bash
   npm install
   ```
3. **Run the Dashboard**:
   ```bash
   npm start
   ```
4. **Access the Dashboard**:
   Visit `http://localhost:3000` (or configured port).

## Vercel Deployment

### Prerequisites
- Vercel account

### Setup Steps
1. **Link Project to Vercel**:
   - Go to [Vercel](https://vercel.com/).
   - Import the GitHub repository.
2. **Configure Environment Variables** in the Vercel Dashboard based on your `.env` file.
3. **Deploy**:
   - After configuration, click on deploy in Vercel.
4. **Visit Deployed Site**:
   - Once deployment is complete, follow the Vercel link provided.

## Testing

### Prerequisites
- Jest or your preferred testing framework installed

### Setup Steps
1. **Navigate to Tests**:
   ```bash
   cd ./tests
   ```
2. **Run Tests**:
   ```bash
   npm test
   ```

---

### Conclusion
This guide covers the essentials for setting up and deploying your project. Ensure to look through each section carefully and customize individual configurations to suit your environment.