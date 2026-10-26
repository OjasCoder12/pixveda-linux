# PixVeda for Linux 🐧

Official Linux release repository for **PixVeda** — the AI-powered study companion and learning assistant for students.

---

## 📥 Download PixVeda for Linux

| File | Version | Size | Architecture | Direct Download |
| :--- | :---: | :---: | :---: | :---: |
| **PixVeda-Linux-x64.tar.gz** | **v1.2.0** | ~11 MB | 64-bit Linux (x86_64) | [⬇️ **Download for Linux**](https://github.com/OjasCoder12/pixveda-linux/releases/latest/download/PixVeda-Linux-x64.tar.gz) |

> 📦 **All Releases & Changelog:** [View Releases](https://github.com/OjasCoder12/pixveda-linux/releases)

---

## 📋 System Requirements

- **Operating System:** Any modern 64-bit Linux distribution (Ubuntu 20.04+, Debian 11+, Fedora 36+, Arch Linux, RHEL 9+, Linux Mint, etc.)
- **Architecture:** 64-bit (x86_64)
- **Desktop Environment:** GNOME, KDE Plasma, XFCE, Cinnamon, etc.
- **Dependencies:** GTK 3 (`libgtk-3`) and libsecret (`libsecret-1`)
- **Internet:** Active connection required for AI tutoring and cloud sync

---

## 🚀 How to Install and Run on Linux

### Step 1: Install Dependencies (If not already installed)
PixVeda utilizes standard GTK 3 and libsecret libraries for secure storage:

- **Ubuntu / Debian / Linux Mint / Pop!_OS:**
  ```bash
  sudo apt update
  sudo apt install -y libgtk-3-0 libsecret-1-0
  ```
- **Fedora / RHEL / CentOS:**
  ```bash
  sudo dnf install -y gtk3 libsecret
  ```
- **Arch Linux / Manjaro:**
  ```bash
  sudo pacman -S gtk3 libsecret
  ```

---

### Step 2: Download and Extract
1. Download `PixVeda-Linux-x64.tar.gz` using the download button above or via curl/wget:
   ```bash
   wget https://github.com/OjasCoder12/pixveda-linux/releases/latest/download/PixVeda-Linux-x64.tar.gz
   ```
2. Extract to your desired directory (for example, `~/PixVeda`):
   ```bash
   mkdir -p ~/PixVeda
   tar -xzf PixVeda-Linux-x64.tar.gz -C ~/PixVeda
   ```

---

### Step 3: Run PixVeda
```bash
cd ~/PixVeda
./pixveda_app
```

---

### 💡 Optional: Add Desktop Shortcut to Application Menu
To launch PixVeda from your system application menu / launcher:

1. Create a desktop entry file:
   ```bash
   cat << 'EOF' > ~/.local/share/applications/pixveda.desktop
   [Desktop Entry]
   Name=PixVeda
   Comment=AI Study Companion for Students
   Exec=/home/$USER/PixVeda/pixveda_app
   Terminal=false
   Type=Application
   Categories=Education;Development;
   EOF
   sed -i "s|\$USER|$USER|g" ~/.local/share/applications/pixveda.desktop
   chmod +x ~/.local/share/applications/pixveda.desktop
   ```
2. PixVeda will now appear in your app launcher!

---

## 🛠️ Troubleshooting & FAQs

### ❓ Error while loading shared libraries
- Ensure `libgtk-3` and `libsecret` packages are installed as shown in Step 1.

### ❓ Permission denied when running `./pixveda_app`
- Mark the binary executable:
  ```bash
  chmod +x ~/PixVeda/pixveda_app
  ```

---

## 🔒 Security & Verification

Verify the integrity of your download:

- **Version:** `1.2.0`
- **File:** `PixVeda-Linux-x64.tar.gz`
- **SHA-256 Checksum:**
  ```text
  3c7b0bcb8b18809dd5ee50fcd54ebf6bf68782cf3b84fea864c15587d94fb51d
  ```

---

## ✨ About PixVeda

PixVeda is an all-in-one AI study companion designed specifically for school and college students:
- 🤖 **AI Chat Tutor:** Step-by-step concept explanations tailored to student grade and syllabus.
- 🗂️ **Interactive Flashcards:** Spaced-repetition study decks to master topics quickly.
- 🧠 **Mind Maps:** Visual diagrams and concept hierarchies generated on the fly.
- ⏱️ **Focus Sessions:** Dedicated study timer with integrated assistance.
- 📝 **Smart Notes & Summarizer:** Convert long documents and textbook chapters into key takeaways.
- 🎯 **Practice Quizzes:** Instant MCQs and test questions with real-time feedback.
- 📅 **Day Planner:** Timetable and guided weekly study plans.
