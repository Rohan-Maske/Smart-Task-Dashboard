Advanced AI-Powered Task Dashboard
📖 Description
This is a commercial-grade, single-page Task Management Dashboard built entirely with frontend technologies. It offers a seamless, real-time, and intelligent user experience for managing tasks without requiring a backend. The application can run in two modes: Local Storage Mode (offline, no setup required) or Firebase Mode (live, collaborative, and persistent data).

This project demonstrates advanced frontend skills, including DOM manipulation, modern JavaScript (ES6+), data management (Firebase/LocalStorage), and integration with external services.

✨ Features
Kanban Board Interface: Organize tasks in To Do, In Progress, and Completed columns.

Drag & Drop: Easily change a task's status by dragging it between columns.

Advanced Task Creation: Add tasks with detailed information including:

Priority Levels (Urgent, High, Medium, Low)

Start Date & Time

Due Date & Time

Descriptive Tags

Intelligent Reminders & Popups:

"Task Starting Soon": A gentle reminder before a task's start time.

"Time Running Out!": An alert if a task's start time has passed but it's not in progress.

"Time's Up!": A final alert when the due date/time is reached.

Snooze Functionality: Delay reminders if you're not ready.

Motivational Quotes: Get random boosts of motivation to keep you productive.

Sound & Browser Notifications: Get native desktop/mobile notifications with sound for all important alerts.

Data Persistence Options:

Firebase Mode: Real-time, collaborative data storage that syncs across devices.

Local Storage Fallback: Works perfectly offline without any setup.

Commercial-Grade Features:

Dark/Light Mode: Switch between themes for your comfort.

Export/Import Data: Backup your tasks to a JSON file and restore them anytime.

Search & Filter: Quickly find tasks by name or priority.

Polished UI/UX:

Smooth animations and transitions.

Helpful tooltips and empty state messages.

Skeleton loaders for a professional loading experience.

Fully responsive design for mobile, tablet, and desktop.

🛠️ Tech Stack
Core: HTML5, CSS3, JavaScript (ES6+)

Styling: Tailwind CSS

Database: Google Firebase (Firestore) / Browser Local Storage

Real-time Communication: Firebase Realtime Listeners

🚀 Getting Started
You can run this project in two ways:

1. Local Mode (Quick & Easy)
No setup is needed! Just download the index.html file and open it in your favorite web browser. The application will automatically detect that Firebase is not configured and will use your browser's local storage to save all your data.

2. Firebase Mode (For Live & Collaborative Features)
To run the application with a live database, follow these steps:

Create a Firebase Project:

Go to the Firebase Console and create a new project.

Add a Web App to your project.

Copy the firebaseConfig object provided.

Set up Firestore:

In your Firebase project, go to Firestore Database and create a new database.

Start in production mode.

Go to the Rules tab and paste the following rules to allow the app to read and write data:

rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /artifacts/{appId}/public/data/{document=**} {
      allow read, write: if true;
    }
  }
}

Publish the rules.

Add Config to index.html:

Open the index.html file.

Find the <script> tag near the bottom of the file.

Replace the placeholder values in the firebaseConfig object with the keys you copied from your Firebase project.

// Before
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  // ...
};

// After
const firebaseConfig = {
  apiKey: "AIzaSy...",
  authDomain: "your-project-id.firebaseapp.com",
  // ...
};

Now, when you open the index.html file, it will connect to your Firebase project and store data online.

📄 License
This project is licensed under the MIT License. See the LICENSE file for details.
