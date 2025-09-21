# Task Dashboard

A modern, responsive task management dashboard with real-time collaboration features, reminders, and motivation system. Built with Firebase (Firestore) for data persistence and CustomTkinter for a sleek UI.

## ✨ Features

- **📝 Task Management**: Create, update, and delete tasks with priorities, due dates, and tags
- **🏗️ Kanban Board**: Drag-and-drop tasks between To Do, In Progress, and Completed columns
- **🔔 Smart Reminders**: Get notifications for upcoming, overdue, and due tasks
- **💬 Real-time Collaboration**: Multiple users can work on tasks simultaneously (Firebase required)
- **🎯 Motivation System**: Periodic motivational quotes to keep you productive
- **🌓 Dark/Light Mode**: Toggle between themes based on your preference
- **📊 Priority System**: Organize tasks with Urgent, High, Medium, and Low priorities
- **📱 Responsive Design**: Works on desktop, tablet, and mobile devices
- **💾 Import/Export**: Backup and restore your tasks with JSON files
- **🔊 Audio Notifications**: Sound alerts for important events

## 🚀 Quick Start

### Option 1: Local Storage Mode (No Setup Required)
1. Download the `index.html` file
2. Open it directly in your web browser
3. Start using the app immediately (data saved in browser's local storage)

### Option 2: Firebase Mode (Real-time Collaboration)
1. Create a Firebase project at [Firebase Console](https://console.firebase.google.com/)
2. Enable Firestore Database in your project
3. Replace the Firebase config in the HTML file:
```javascript
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_PROJECT_ID.appspot.com",
  messagingSenderId: "YOUR_SENDER_ID",
  appId: "YOUR_APP_ID"
};
```
4. Set up Firestore security rules (optional but recommended)
5. Open the HTML file in your browser

## 📁 Project Structure

```
task-dashboard/
└── index.html      # Main application file
└── LICENSE         # License
└── README.md       # Document
```

## 🎯 Usage

### Creating Tasks
1. Click the "New Task" button
2. Fill in task details (title, description, priority, dates, tags)
3. Click "Save Task" to add it to your board

### Managing Tasks
- **Drag & Drop**: Move tasks between columns to update their status
- **Checkbox**: Mark tasks as complete/incomplete
- **Delete**: Click the trash icon to remove tasks
- **Search**: Use the search bar to find specific tasks
- **Filter**: Filter tasks by priority level

### Notifications & Reminders
- The app will show popup reminders for:
  - Tasks starting soon (5-minute warning)
  - Overdue tasks that haven't been started
  - Tasks that are past their due date
- Click "Snooze" to postpone reminders for 5 minutes
- Click action buttons to directly update task status

### Theme Switching
Click the theme toggle button to switch between dark and light modes. Your preference is saved automatically.

## 🔧 Technical Details

### Built With
- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **Styling**: Tailwind CSS
- **Backend**: Firebase Firestore (optional)
- **Icons**: Heroicons (SVG)
- **Notifications**: Web Notifications API

### Browser Compatibility
- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

### Data Persistence
- **Local Mode**: Uses browser's Local Storage
- **Firebase Mode**: Real-time synchronization across devices

## 📦 Import/Export

### Exporting Tasks
1. Click the export button (download icon)
2. A JSON file containing all your tasks will be downloaded
3. Keep this file as a backup

### Importing Tasks
1. Click the import button (upload icon)
2. Select your previously exported JSON file
3. Confirm to overwrite current tasks (this action cannot be undone)

## 🔐 Privacy & Security

- **Local Mode**: All data stays on your device
- **Firebase Mode**: Data is stored securely in Firebase's servers
- No personal data is collected without your consent
- You can export and delete your data at any time

## 🐛 Troubleshooting

### Common Issues
1. **Notifications not working**: Ensure your browser allows notifications
2. **Firebase connection errors**: Check your Firebase configuration
3. **Drag and drop not working**: Try refreshing the page

### Getting Help
If you encounter issues:
1. Check the browser console for error messages (F12)
2. Ensure you have a stable internet connection (for Firebase mode)
3. Try using Local Storage mode if Firebase isn't working

## 🤝 Contributing

Feel free to fork this project and submit pull requests for improvements. Some areas for enhancement:
- Additional task filters
- Custom notification sounds
- Task categories/projects
- Calendar view integration
- Task templates

---

**Note**: This application works best in modern browsers with JavaScript enabled. For the best experience, use the latest version of Chrome, Firefox, or Safari.
