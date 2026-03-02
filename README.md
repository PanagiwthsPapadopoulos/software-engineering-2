# OnlyVibes: Full-Stack Social Event Discovery 🪩

**OnlyVibes** is a comprehensive social platform designed to bridge the gap between local event organizers and discovery-seeking users. Built with a mobile-first philosophy, it enables users to create, manage, and review local happenings in real-time.



## 🏗️ System Architecture

The ecosystem is built on a decoupled architecture, separating a high-performance React client from a robust Express/MongoDB API.

### **Frontend: React Interface**
* **Mobile-First UX**: Tailored for on-the-go discovery with a bottom navigation bar and touch-friendly event cards tailored for mobile viewports.
* **Optimistic UI**: Implements "Optimistic Updates" for likes and unlikes to ensure a highly responsive user experience.
* **State & Auth**: Features a secure authentication flow using JWT tokens stored in LocalStorage, supporting both full access and a restricted "Guest Mode" for browsing.
* **Screen Coverage**: Includes over 9 specialized screens, including a Profile Dashboard, Event Creation/Editing forms, and a Search interface.

### **Backend: Express & MongoDB API**
* **Architectural Pattern**: Follows a strict Controller-Service-Model structure to ensure a clear separation of concerns and maintainable request flows.
* **Validation & Security**: Features multi-layered request validation for all endpoints, Bcrypt password hashing, and custom JWT verification middleware.
* **Reliability**: Implements centralized error handling and database health probes (`dbHealth`) to provide consistent JSON responses and system stability.

## 🛠️ Tech Stack & Tooling

| Layer | Technologies |
| :--- | :--- |
| **Frontend** | React (v18), Vite, Axios, React Router v6, CSS Modules, Lucide React |
| **Backend** | Node.js (v18+), Express 5, Mongoose 8, JWT, Bcrypt |
| **Database** | MongoDB (Atlas / In-Memory for testing) |
| **Testing** | **Cypress** (E2E Frontend), **Jest & Supertest** (Backend Integration) |
| **DevOps** | **GitHub Actions** (CI/CD), **Render** (Production Deployment) |

## 🧪 Quality Assurance & DevOps

OnlyVibes was built with a "Shift-Left" testing mentality to ensure mission-critical workflows are always verified before reaching production.

* **Automated Testing**: The backend maintains ≥80% coverage across 140+ Jest scenarios, while the frontend utilizes Cypress to automate three distinct user flows (Auth, Events, and Reviews).
* **CI/CD Pipeline**: Configured via GitHub Actions to spin up virtual environments and execute the full test suite on every push; deployment to **Render** is strictly blocked if any test fails.
* **Static Analysis (Cyclopt)**: The project achieved a 100% clean-code rating with **0 violations**, **0 vulnerabilities**, and **0% duplicate code**, meeting the highest standards for modularity and security.

## ➕ More Information

You can find more information about each project (frontend/backend) separately in the READMEs of each one.
