# GradeWise AI - Front-End Demo

This repository contains the front-end HTML, CSS, and basic JavaScript code for a demonstration version of **GradeWise AI**, a web application concept designed to assist educators in grading student papers using AI.

**Live Demo URL:** (Optional: Add the URL here if you deploy it using GitHub Pages, Netlify, Vercel, etc.)

## Project Goal

The aim was to build the user-facing web pages for GradeWise AI, including:
*   A marketing landing page.
*   User authentication forms (Login/Signup).
*   Mockups of core application sections (Dashboard, Projects, Account Settings, API Key Management).
*   A functional, interactive demo of the core AI grading feature using a live API call to Google Gemini.

## ⚠️ Project Status & Disclaimer

This is currently a **front-end only demonstration**.
*   It primarily uses static HTML pages styled with Tailwind CSS.
*   JavaScript is used for basic interactivity (mobile menu, tabs, smooth scroll) and **one functional API call** in the demo page.
*   **There is no backend database or server-side logic.** User authentication is not functional, and data entered into simulated forms (like adding projects, contacts, or API keys in `gradewise_demo.html`) is **not saved** beyond the current browser session.
*   **The API call in `gradewise_demo.html` uses a hardcoded key and is INSECURE for public deployment.** (See Security Warning below).

## ✨ Key Features Demonstrated/Mocked Up

*   **Landing Page (`aiiii.html`):** Introduces the concept, highlights features (AI Grading, BYOK, Batch Grading), previews pricing.
*   **Interactive Grading Demo (`gradewise_demo.html`):**
    *   Allows uploading/pasting grading criteria.
    *   Allows uploading a student paper.
    *   Makes a **live call** to Google Gemini API for grading (using a hardcoded key).
    *   Displays AI-generated feedback and score.
    *   Includes simulated sidebar navigation to other application sections (Projects, API Keys, etc.) within the same page.
    *   Modernized GUI for the grading interface.
    *   Dark Mode toggle (specific to this page).
*   **Pricing Page (`plans.html`):** Compares different subscription tiers.
*   **Authentication (`login.html`, `signup.html`):** Standard login and registration forms (front-end only).
*   **Mockup Pages:** Visual representations (no backend functionality) for:
    *   `dashboard.html`: Post-login overview.
    *   `projects.html`: Managing grading assignments.
    *   `apikeys.html`: Managing user's own API keys (BYOK).
    *   `account.html`: User profile, password, subscription settings using tabs.

## 💻 Technology Stack

*   **HTML5**
*   **Tailwind CSS v3** (via CDN)
*   **Vanilla JavaScript** (for DOM manipulation, basic interactivity, API fetch, `localStorage` for dark mode)
*   **Google Fonts** (Inter)
*   **Lucide Icons** (Font via CDN)
*   **Google Gemini API** (Called directly from `gradewise_demo.html`'s JavaScript - **INSECURE DEMO IMPLEMENTATION**)

## 📂 File Structure Overview

*   `aiiii.html`: Main marketing/landing page. Links to all other pages. (Consider renaming to `index.html` for deployment).
*   `gradewise_demo.html`: The core interactive demo page, including the functional grading tool and simulated sections toggled via the sidebar. **Contains the insecure hardcoded API key.**
*   `plans.html`: Detailed pricing plan comparison.
*   `login.html`: User login form.
*   `signup.html`: User registration form.
*   `dashboard.html`: Mockup of the main user dashboard.
*   `projects.html`: Mockup for managing grading projects.
*   `apikeys.html`: Mockup for managing user API keys (BYOK).
*   `account.html`: Mockup for user account settings (Profile, Password, Subscription, Preferences).

*(Optional: Add any CSS or JS folders/files if you created separate ones)*
*   `(images/)`: (If you use local images like `placeholder1.png`, ensure they exist).

## 🚨🚨 CRITICAL SECURITY WARNING - API KEY 🚨🚨

The file `gradewise_demo.html` contains a **hardcoded Google Gemini API key** within its `<script>` tag:

```javascript
// --- Hardcoded API Key (INSECURE - For Demo Only) ---
// Replace with your actual key for local testing. Disable key afterwards.
const HARDCODED_API_KEY = "AIzaSyClI8VW8G6_RdGQuse5dAUxHtefVke1qjc"; // EXAMPLE KEY
// --- End Hardcoded API Key ---