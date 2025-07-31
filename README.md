Digital E-Gram Panchayat – Next-Generation Digital Governance Platform
<div align="center">
![Digital E-Gram Panchayat](https://img.shields.io/badge/Digital-E--Gram%20Panchayat-blue?style=for://img.shields.io/badge/React-18.3.1-61DAFB?style=for-the-badge](https://img.shields.io/badge/TypeScript-5.5.3-3178C6?style=for-the-badge&logo://img.shields.io/badge/Firebase-10.13.0-FFCA28?style=for-the-badge&logo=firebase](https://img.shields.io/badge/Tailwind%20CSS-3.4.10-06B6D4?style=for-the-badge&logo platform uniting village residents with digital government services. Citizens can apply, monitor requests, and access support, while staff and officials efficiently oversee service delivery and workflow.**

🚀 Live Demo - 📖 Documentation - 🐛 Report Bug - ✨ Request Feature

</div>
📋 Contents
🎯 Overview

✨ Features

🛠️ Tech Stack

🚀 Quick Start

📁 Project Structure

🔧 Development Workflow

🌐 Deployment

🔐 Environment Variables

📱 Usage Guide

🎨 Design System

🧪 Testing

🤝 Contributing

📄 License

👨💻 Developer

🎯 Overview
Digital E-Gram Panchayat modernizes rural governance with a user-friendly, responsive web portal. The platform lets citizens apply for services, manage their cases, and track updates, streamlining administrative work for government staff.

🎨 Design Approach
Cutting-edge UI/UX: Visual polish and interactive transitions on par with leading web builders.

Accessibility-Centric: WCAG 2.1 standards adherence and comprehensive keyboard support.

Responsive by Default: Optimized layouts for mobile, tablet, and desktop.

Performance First: Fast load times and fluid navigation.

🏛️ Government Alignment
Role-Specific Access: Distinct citizen, staff, and admin views with tailored permissions.

Secure Sign-In: Firebase email authentication with verification mechanics.

Document Workflows: Safeguarded handling and storage for submitted paperwork.

Audit Log: Thorough event tracking for transparency.

✨ Main Features
⚡ Core Capabilities
👥 For Citizens
📝 Online Filing: Apply for government services via digital forms.

📊 Track Requests: Monitor application progress in real-time.

🔔 Automated Email Updates: Get notified about changes in status.

👤 Personal Area: Maintain secure account details and documents.

📱 Optimum Mobile Experience: Full functionality on any device size.

👨💼 For Staff
📋 Application Oversight: Manage requests from a unified dashboard.

✅ Lifecycle Updates: Record actions, update status, and leave notes.

📈 Analytics Tools: Monitor service metrics and staff productivity.

🔍 Advanced Search: Filter and locate applications swiftly.

🔧 For Admins
🛠️ Service Oversight: Add, edit, categorize, or retire offered services.

👥 User Roles: Manage users and control access levels.

📊 Platform Stats: Generate system-wide analytics and reports.

⚙️ Custom Setup: Configure app-wide preferences.

🎨 UI/UX Additions
🌙 Dark/Light Themes: Easily switch (or auto-detect) based on user/system preference.

✨ Smooth Transitions: Page and micro interaction animation powered by Framer Motion.

🎭 Modern Visual Effects: Glassmorphism, backdrop blur, and more.

🎨 Consistent Styles: Cohesive palette, typography, and scale.

📱 PWA Ready: Offline accessibility and home screen installation.

🔒 Security Safeguards
🔐 Reliable Authentication: Email sign-in via Firebase Auth.

🛡️ Role Checks: Permissions enforced based on user type.

📝 Activity Monitoring: Actions logged for compliance.

🔒 Secure Data: All data encrypted at rest and in transit.

🚫 Robust Validation: Input checks at both client and backend layers.

🛠️ Tech Overview
Frontend
Framework: React 18.3.1 + TypeScript

Development Build: Vite 5.4.1

Styles: Tailwind CSS 3.4.10, custom configuration

Animations: Framer Motion 10.16.4

Icons: Lucide React 0.441.0

Routing: React Router DOM 6.26.1

Backend & Cloud
Sign-In: Firebase Auth 10.13.0

Database: Cloud Firestore, realtime updates

Hosting: Firebase Hosting

Emails: EmailJS

Backend Logic: Firebase Functions

Developer Tools
Type Checking: TypeScript 5.5.3

Linting: ESLint 9.9.0

Package Manager: npm

Source Control: Git (with conventional commits)

Design & UI
Design System: Custom Tailwind config

Typography: Inter & Poppins font pairing

Color System: Extensive color ramps with dark mode

Mobile-First Design

Accessibility: WCAG 2.1 AA-based

🚀 Quick Start
Prerequisites
Verify you have:

Node.js (16.0.0+)

npm (7.0.0+, included with Node)

Git

Firebase Account

EmailJS Account

Setup Steps
Clone Repository

bash
   git clone https://github.com/your-username/digital-egram-panchayat.git
   cd digital-egram-panchayat
Install Packages

bash
   npm install
Copy Environment Template

bash
   cp .env.example .env
Configure .env
Edit your new .env file:

text
VITE_FIREBASE_API_KEY=...
VITE_FIREBASE_AUTH_DOMAIN=...
...
VITE_EMAILJS_SERVICE_ID=...
...
   VITE_ENABLE_LOGGING=false
Start Local Development

bash
   npm run dev
Open in Browser
Head to http://localhost:5173

Firebase Steps
Create Project

Visit the Firebase Console, create a project, enable Auth & Firestore.

Setup Authentication

Activate Email/Password sign-in and check allowed domains.

Firestore Setup

Set up Firestore, launch in production mode, apply your own security rules.

Deploy Firestore Settings

bash
   npm run firebase:deploy
EmailJS Setup
Sign Up at EmailJS

Register and add a new email service.

Create Templates

For contact, OTP, and notifications.

Get Credentials

Service ID, Template IDs, and Public Key go in your .env.

📁 Directory Overview
text
digital-egram-panchayat/
├─ public/
│  ├─ vite.svg
│  └─ index.html
├─ src/
│  ├─ components/
│  │  ├─ ui/ (Button, Card, Input, Modal, etc.)
│  │  ├─ layout/ (Header, Footer)
│  │  └─ Common/ (LoadingSpinner, ProtectedRoute, StatusBadge)
│  ├─ pages/ (Home, Login, Register, Services, Apply, Profile, About, Contact, Terms, Privacy, NotFound, Unauthorized, dashboards)
│  ├─ services/ (auth, applications, services, logging, emailService, otpService)
│  ├─ context/ (AuthContext)
│  ├─ hooks/ (useTheme)
│  ├─ lib/ (utils)
│  ├─ types/ (index)
│  ├─ firebase/ (config)
│  ├─ App.tsx, main.tsx, index.css, vite-env.d.ts
├─ firebase/ (firestore.rules, firestore.indexes.json, firebase.json)
├─ package.json
├─ tailwind.config.js
├─ tsconfig.json
├─ vite.config.ts
├─ .env.example
├─ .gitignore
├─ README.md
🔧 Workflow Basics
Key npm Scripts
bash
npm run dev              # Launch dev server
npm run build            # Production build
npm run preview          # Preview final build
npm run lint             # Lint code

npm run firebase         # Firebase CLI
npm run firebase:emulators   # Run emulators
npm run firebase:deploy  # Deploy app
Development Steps
Add a Feature

bash
git checkout -b feature/your-feature
# Make changes, then:
   git add .
git commit -m "feat: add ..."
git push origin feature/your-feature
# Submit PR
Enhancing Quality

TypeScript best practices

Linting with ESLint

Conventional commit messages

Testing Builds

bash
   npm run lint
   npm run build
   npm run preview
Git Strategy
Follows Git Flow model:

main: production

develop: staging integration

feature/*: new features

hotfix/*, release/*: urgent fixes/releases

Commit Style
Example commit types:

text
feat: implement OTP for registration
fix: persist auth state
docs: clarify deployment steps
style: revise button hover
refactor: clean app service queries
test: add auth unit tests
chore: update dependencies
🌐 Deployment
Firebase Hosting
Build App

bash
   npm run build
Deploy

bash
   npm run firebase:deploy
(Optional) Custom Domain

Add domain via Firebase Hosting, set up DNS, and SSL.

Per-Environment Deployments
Dev

bash
firebase use development
npm run firebase:deploy
Prod

bash
firebase use production
npm run firebase:deploy
Deployment Checklist
 Environment variables set

 Firebase ready

 Firestore rules/application deployed

 Authentication up

 EmailJS templates in place

 Domain DNS/SSL done (if applicable)

 Performance tested

Monitoring Tools
Firebase Analytics: usage insights

Performance tools: Core Web Vitals

Error logging

Periodic security audits

🔐 Environment Variables
.env Variables
text
# Firebase config
VITE_FIREBASE_API_KEY=...
VITE_FIREBASE_AUTH_DOMAIN=...
VITE_FIREBASE_PROJECT_ID=...
VITE_FIREBASE_STORAGE_BUCKET=...
VITE_FIREBASE_MESSAGING_SENDER_ID=...
VITE_FIREBASE_APP_ID=...

# EmailJS config
VITE_EMAILJS_SERVICE_ID=...
VITE_EMAILJS_TEMPLATE_ID=...
VITE_EMAILJS_OTP_TEMPLATE_ID=...
VITE_EMAILJS_PUBLIC_KEY=...

# Dev settings
VITE_ENABLE_LOGGING=false
VITE_USE_FIREBASE_EMULATOR=false
How to Find Keys
Firebase: Firebase Console › Project Settings › Web App Config

EmailJS: EmailJS Dashboard › Service & Template IDs, Public Key

Security Tips:

Never commit .env in Git

Use separate prod/dev settings

Rotate secrets often

Apply strong Firestore rules

Use App Check for extra protection

📱 User Guide
Citizens
Signup Flow
Go to /register

Fill in personal info

Enter OTP from verification email

Finish and auto-sign in

Applying for a Service
See options at /services

Hit "Apply Now" for the service you need

Fill paperwork, review, submit

See updates on your account dashboard

Dashboard
View request statuses

Get real-time status changes

Upload documents

Edit your info

Staff
Review Requests
Log in to staff dashboard

View open case files

Update progress/status with notes

Communicate with applicants as needed

Workflow Tools
Filter/search applications

Bulk actions on cases

See analytics or generate reports

Admins
Manage Services
Add/edit/delete any type of service

Specify documentation, costs, and categories

Control visibility/activation

Users & Roles
Assign staff/admins

Track activity logs

Handle permissions and oversight

Demo Credentials
text
Admin:    admin@demo.com / password
Staff:    staff@demo.com / password
Citizen:  citizen@demo.com / password
🎨 Design System
Colors
Primary (Blues):

primary-50: #eff6ff … primary-950: #172554

Secondary (Grays/Indigo):

secondary-50: #f8fafc … secondary-950: #020617

Semantic: Green (Success), Yellow (Warning), Red (Error), Orange (Accent)

Fonts
Headings: Poppins

Body Text: Inter

Weights: 300–900 for a flexible hierarchy

Size Scale (examples):

xs: 12px, sm: 14px, base: 16px, lg: 18px, xl: 20px, 2xl: 24px, ... up to 6xl: 60px

Spacing (8px grid):
0 = 0px, 1 = 4px, 2 = 8px, etc., up through 32 (128px).

Component Basics
Buttons: Types for action (primary/secondary/outline/ghost)

Cards: 12px radius, 24px padding, subtle shadows

Forms: 48px heights, clear errors, 8px label-input spacing

Animations
Easing and timing: ease-out (show), ease-in (hide), ease-in-out (change), durations from 150ms (fast) to 500ms (deliberate)

🧪 Testing Strategy
What’s Tested
Unit: Components, services, utilities

Integration: Workflows and API interactivity

E2E: Key user paths, cross-browser usability, responsive behaviors

How to Test
bash
npm test
npm run test:watch
npm run test:coverage
npm test -- Button.test.tsx
Test Focus
Actions from a user’s viewpoint

Accessibility (screen readers, etc.)

All error/edge conditions

Speed and load checks

Manual Test Checklist
Auth – registration, login, password resets, session persistence

Application – browse, submit, upload, get notified

Responsive – mobile, tablet, desktop, keyboard nav

Accessibility – contrast, focus rings, alt text

🤝 Contribution Guide
Contributions are valued! Here’s what to do:

How to Start
Fork and Clone



bash
git checkout -b feature/new-feature
Develop

Keep code style consistent

Add and document tests

Update/readme as needed

Commit Clearly

bash
git commit -m "feat: your feature"
Push & PR

bash
git push origin feature/new-feature
Create a pull request, describing changes and linking issues/screenshots.

Standards & Process
Use TypeScript and ESLint

Clear commit messages (Conventional Commits)

JSDoc where helpful

Semantic HTML

PR Checklist
Thorough README or docs updates

Increment version as needed

All tests must pass

Wait for maintainer feedback/approval

Reporting Issues
Use provided templates

Steps to reproduce, environment info, labeling

Dev Setup for Contributors
Install deps: npm install

Set up pre-commit: npm run prepare

Run dev: npm run dev

Run tests: npm test

Where to Help
🐛 Bug squashing

✨ New features

📚 Documentation

🎨 UI polish

♿ Accessibility

🌐 Language/internationalization

🔧 Performance work

🧪 Testing improvements

📄 License
This software is shared under the MIT License (see LICENSE for details).

You Can:

Use for business or personal projects

Modify and distribute

Fork and adapt

You Can’t:

Hold the author liable

Expect a warranty

👨💻 About the Developer
<div align="center">
Sanket Deka
Full-Stack Developer & UI/UX Specialist


</div>
About Sanket Deka
Hey there! I'm currently studying AI & ML at Universal AI University, and I love turning tech ideas into real solutions.

I’ve built Arduino-based robots, worked with sensors for smart fire-fighting, and I’m now exploring advanced machine learning and real-time data.

Always excited to collaborate, innovate, and make an impact. 

Competency Areas
Frontend: React, TypeScript, Tailwind, Framer Motion

Backend: Node.js, Firebase, Express

Design: UI/UX, mobile optimization, accessible interfaces

Toolset: Git, Figma, Firebase, Netlify, Vercel

Contact
Email: sanket.dekaglgt@gmail.com


LinkedIn: Sanket Deka

GitHub: krishna142-tech

📞 Help & Contact
Where to Get Answers
📖 Documentation: Refer to this README and the code itself.

🐛 Bugs: Report using Issues

💡 Features: Suggest enhancements in Issues

💬 Chat: Join the Discussions

Quick Links
🚀 Live: App Home

📂 Repo: GitHub

📋 Project Board: Projects

📊 Analytics: Firebase Console

<div align="center">