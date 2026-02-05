# SaaS Consultation App (Vercel Serverless Edition)

![Next.js](https://img.shields.io/badge/Next.js-16.1.6-black?style=for-the-badge&logo=next.js)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.12-3776AB?style=for-the-badge&logo=python&logoColor=white)

A serverless-first SaaS template designed for the Vercel ecosystem. This version leverages Vercel’s native ability to run both a React frontend and Python backend functions in a distributed, zero-config environment.

## 🧠 How It Works: Serverless Integration
This repository is structured to take advantage of Vercel’s "Zero Config" deployments:
1. Frontend: Next.js handles the UI and client-side routing.
2. Backend: Any Python files placed in the /api directory are automatically detected by Vercel and deployed as independent Serverless Functions.
3. Proxying: During development, the Next.js dev server automatically proxies requests to the Python backend, allowing you to build the entire app locally with one command.

## ✨ Key Features
- Speed: Next.js 16 with Turbopack for lightning-fast development iterations.
- Scalability: Serverless Python functions scale to zero when not in use, saving costs.
- Auth: Clerk integration provides a seamless "Sign In / Sign Up" flow out of the box.
- Modern UI: Tailwind CSS 4.0 for utility-first styling and rapid prototyping.

## 📂 Project Structure
- /api: Python serverless functions (each file represents a route).
- /pages: Next.js frontend using the Pages router.
- /styles: Global CSS and Tailwind configurations.
- requirements.txt: Python dependencies for the serverless backend.

## ⚡ Local Development

1. Install Dependencies:
npm install
pip install -r requirements.txt

2. Environment Config:
Add your Clerk keys to .env.local:
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=pk_test_...
CLERK_SECRET_KEY=sk_test_...

3. Launch:
npm run dev
The app will be available at http://localhost:3000.

## 🚀 Deployment
1. Connect your GitHub repository to Vercel.
2. Vercel will auto-detect Next.js and the Python /api folder.
3. Add your Environment Variables in the Vercel dashboard.
4. Deployment happens automatically on every 'git push'.

---
Created by Jonathan Feagans