# Learn Tracker 

A responsive single-page study tracker for a 26-week software-engineering job switch plan. It includes daily tasks, pattern-first DSA, a 150-item problem bank, backend/cloud milestones, weekly reflections, and recovery for missed days.

## Run locally
Open `index.html` in a modern browser. In demo mode, progress is stored in that browser only.

## Enable cross-device sync with Firebase
1. Create a Firebase project at https://console.firebase.google.com/
2. Add a Web App and copy its config into `index.html` where `firebaseConfig` is defined.
3. In **Authentication → Sign-in method**, enable **Google**.
4. In **Authentication → Settings → Authorized domains**, add your GitHub Pages domain (for example `YOUR_GITHUB_USERNAME.github.io`).
5. Create a **Cloud Firestore** database.
6. Apply the security rules in `firestore.rules`.
7. Commit the config change and sign in with the same Google account on laptop and mobile.

Firebase web config is not a server secret. The Firestore rules are essential: they limit each signed-in user to their own tracker document.

## Deploy to GitHub Pages
1. Create a public repository named `learn-tracker`.
2. Upload `index.html`, `README.md`, and `firestore.rules` to the repository root.
3. In **Settings → Pages**, choose **Deploy from a branch**, select `main` and `/ (root)`, then Save.
4. Wait for GitHub Pages to publish. The URL will be `https://YOUR_GITHUB_USERNAME.github.io/learn-tracker/`.

## Notes
- Plan start date defaults to **November 2, 2026**; change it in the dashboard if needed.
- Weekdays use a 60-minute structure; weekends use two focused blocks.
- The curated problem list is a study sequence; problem links currently point to LeetCode's problemset. Add exact problem URLs as you personalize the bank.
- This is a static site; Firebase provides auth and sync. No server or secrets are hosted in the repository.
