# 🌐 **LinuxHub**
### _Learn Linux the Smart Way — One Lesson at a Time_

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Android-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Version-1.0.0-green?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Status-Active-success?style=for-the-badge" />
  <img src="https://img.shields.io/badge/License-MIT-lightgrey?style=for-the-badge" />
</p>

---

## 🚀 About LinuxHub
**LinuxHub** is a beginner-friendly Android learning app designed to teach Linux step by step.  
It provides structured lessons, real command examples, in-app videos, and guidance without overwhelming new learners.

If you're someone who wants to understand Linux from scratch — **this app is made for you.**

---

## 📱 Key Features
- 📚 Beginner-focused Linux lessons  
- 💡 Real command examples (`ls`, `pwd`, `cd`, etc.)
- ▶️ YouTube lessons inside the app (no external browser)
- 🔔 Firebase push notifications for new topics
- 🔄 Auto-fetches updated content from GitHub
- 🔐 Lesson integrity protected with SHA-256 hash validation
- 🧭 Simple, clean UI made for learners

---

## 🧩 How the App Works
```
Android App
    ↓
Loads index → cloud_linux_classes_index.json
    ↓
Fetches lesson files → class_<ID>_content.json
    ↓
Displays lesson (text + commands + video)
```

---

## 📂 Project Structure

```
LinuxHub/
│
├── classes/
│   ├── class_1_content.json
│   ├── class_2_content.json
│   ├── ...
│   ├── cloud_linux_classes_index.json   # All lessons listed here
│
├── txt_classes/                         # Raw lesson sources before processing
│
├── scripts/
│   └── update-class-hashes.ps1          # Generates SHA256 and updates index
│
├── app/                                 # Android source code
│
└── README.md
```

---

## 🌐 Content Fetch URLs (Used by App)

| Purpose | URL |
|--------|-----|
| Index file | `https://raw.githubusercontent.com/mrlinux-in/LinuxHub/main/classes/cloud_linux_classes_index.json` |
| Class file format | `https://raw.githubusercontent.com/mrlinux-in/LinuxHub/main/classes/class_<ID>_content.json` |

Example:
```
https://raw.githubusercontent.com/mrlinux-in/LinuxHub/main/classes/class_1_content.json
```

---

## 🔄 Content Update Workflow

1. Add/edit text in `txt_classes/classX.txt`
2. Run Python script to generate JSON
3. Run hash script:
   ```powershell
   ./scripts/update-class-hashes.ps1
   ```
4. Commit & push to GitHub
5. The app automatically pulls new content

---

## 🛠️ Development Setup

### Clone the repo
```bash
git clone https://github.com/mrlinux-in/LinuxHub.git
cd LinuxHub
```

### Update lesson hashes
```powershell
.\scripts\update-class-hashes.ps1
```

### Open in Android Studio
```
File → Open → Select project folder → Run
```

---

## 🔥 Roadmap
- [ ] Offline lesson mode
- [ ] Fullscreen & improved video player
- [ ] Progress tracking & profiles
- [ ] In-app quizzes and practice tasks
- [ ] Terminal simulation (beginner safe)
- [ ] Shareable certificates for completion

---

## ❤️ Contributing
We welcome:
- 🐞 Bug reports
- 💡 Feature suggestions
- 📚 Lesson content improvements
- 🤝 Pull requests

Open an issue or PR anytime!
👉 https://github.com/mrlinux-in/LinuxHub/issues

---

## 📄 License
This project is available under the **MIT License**.  
Feel free to use, modify, improve & share.

---

## ⭐ Support the Project
If you like LinuxHub or want more lessons:
**Please star the repo! It really helps.**

👉 https://github.com/mrlinux-in/LinuxHub ⭐

---

<p align="center">
  Made with ❤️ for Linux learners  
</p>
