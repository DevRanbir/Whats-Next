<!-- PROJECT IMAGE / BANNER -->
<p align="center">
  <img width="100%" alt="Screenshot 2026-01-24 015627" src="https://github.com/user-attachments/assets/8d7dc71c-5d6d-4cc4-a74e-140583abaa2c" />

</p>

# What's Next
Your smart campus companion - Know where your friends are and what's happening next.

---
<img width="18%" alt="Screenshot_20260124_014736" src="https://github.com/user-attachments/assets/110464c3-b3a9-4f8e-a692-24d184f8e862" />
<img width="18%" alt="Screenshot_20260124_014700" src="https://github.com/user-attachments/assets/979a07bf-69d0-404d-b944-859f8362f2ad" />
<img width="18%" alt="Screenshot_20260124_014235" src="https://github.com/user-attachments/assets/9772a486-4485-46f7-9eee-007c7e0d5f0c" />
<img width="18%" alt="Screenshot_20260124_014624" src="https://github.com/user-attachments/assets/92b22e0b-640a-4df9-addd-8420f93b123a" />
<img width="18%" alt="Screenshot_20260124_014337" src="https://github.com/user-attachments/assets/a40e993c-44a6-46aa-b506-b62f56ef26de" />

---

## 📖 Description

What's Next is a comprehensive Android application designed to revolutionize the campus experience for university students. It seamlessly integrates academic utilities with social connectivity, solving the everyday challenge of coordinating with friends across a busy campus.

**What problem it solves:**
- Never miss meeting up with friends during free periods
- Eliminate the hassle of manually checking and comparing timetables
- Stay connected with your campus social circle in real-time

**What makes it unique:**
- Automated timetable sync from university portals with intelligent free period detection
- Real-time friend status tracking showing who's free, in class, or at lunch
- QR code-based instant friend pairing with home screen widgets for quick access

---

## ✨ Features

- **Smart Free Period Detection** – Identifies gaps between classes and highlights available time slots
- **Real-Time Friend Status** – See where your friends are (In Class, Free, Lunch) with live updates
- **QR Code Friend Pairing** – Instantly add friends by scanning unique QR profile codes
- **Pinned Friends Widget** – Quick home screen access to your closest friends' status
- **Offline Access** – Cached timetable and profile data for viewing without internet
- **Google Sign-In Integration** – Secure authentication with automatic student ID verification

---

## 🧠 Tech Stack

**Android Development**
- Kotlin
- Jetpack Compose (Material3)
- MVVM Architecture
- Coroutines & Flow

**Backend & Database**
- Firebase Authentication
- Firebase Realtime Database
- Firebase Cloud Messaging (FCM)


**AI / ML**
- Google ML Kit (Text Recognition for OCR)
- ML Kit Barcode Scanning
- ZXing (QR Code generation)

**UI & Media**
- CameraX
- Lottie Animations
- Accompanist (System UI & Permissions)

---

## 🏗️ Architecture / Workflow

```text
User → UI (Jetpack Compose) → ViewModel → Repository → Data Sources
                                                          ├── Firebase (Auth, RTDB, FCM)
```

---

## ⚙️ Installation & Setup

```bash
# Clone the repository
git clone https://github.com/yourusername/whatsnext.git

# Navigate to project
cd whatsnext/android_app

# Open in Android Studio
# Sync Gradle files

# Run on emulator or device
./gradlew installDebug
```

**Requirements:**
- Android Studio Hedgehog or later
- Minimum SDK: 24
- Target SDK: 34
- Kotlin 1.9+

---

## 🔐 Environment Variables

Create a `google-services.json` file in the `app/` directory:

1. Create a Firebase project in the [Firebase Console](https://console.firebase.google.com/)
2. Add an Android app with package name from your `build.gradle.kts`
3. Download `google-services.json`
4. Enable Firebase Authentication (Google Sign-In) and Realtime Database

Optional: Create `key.properties` for release signing:

```properties
storePassword=your_store_password
keyPassword=your_key_password
keyAlias=your_key_alias
storeFile=path_to_keystore.jks
```

---

## 🧪 Usage

**Step 1:** Launch the app and sign in with your Google account

**Step 2:** Complete the interactive onboarding flow to link your student ID

**Step 3:** The app automatically syncs your timetable from the university portal

**Step 4:** Add friends via QR code scanning or friend requests

**Step 5:** View real-time status of friends and discover free periods to meet up

**Step 6:** Pin important friends to your home screen widget for instant access

---

## 🎥 Demo

* **Live Demo:** Coming Soon
* **Screenshots:** Coming Soon

---

## 📂 Project Structure

```text
android_app/
├── app/
│   ├── src/
│   │   └── main/
│   │       ├── kotlin/
│   │       │   └── com/example/whatsnext/
│   │       │       ├── data/
│   │       │       │   ├── model/          # Data classes (ClassSession, Profile, etc.)
│   │       │       │   └── repository/     # Business logic & Data fetching
│   │       │       │       ├── PortalRepository.kt  # Portal scraping
│   │       │       │       ├── FriendRepository.kt  # Friend management
│   │       │       │       └── AuthRepository.kt    # Authentication
│   │       │       ├── ui/
│   │       │       │   ├── components/    # Reusable Composables
│   │       │       │   ├── screens/       # Feature screens
│   │       │       │   └── theme/         # Design system
│   │       │       ├── utils/             # Helper functions
│   │       │       └── widget/            # Home screen widgets
│   │       └── res/
│   ├── build.gradle.kts
│   └── google-services.json
├── build.gradle.kts
└── settings.gradle.kts
```

---

## 👥 Team / Author

* **Project:** What's Next
* **Platform:** Android
* **Status:** In Development

---

## 📜 License

This project is for educational and personal use. 

---

## 🔍 Technical Highlights

### Adaptive Navigation
Features a unique bottom navigation system that morphs between modes:
- **Standard Mode:** Full navigation with Profile, Home, Friends, Settings
- **Onboarding Mode:** Simplified flow synchronized with setup progress

### Real-Time Sync
Leverages Firebase Realtime Database for:
- Low-latency friend status updates
- Instant timetable synchronization across devices
- Push notifications for friend requests and status changes
