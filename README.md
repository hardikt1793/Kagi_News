
## You can watch the demo of the app in action here:

[![Watch the video]]

https://github.com/user-attachments/assets/43999284-a3ca-48c1-b642-7a67ea0909d6

# 📰 Kites News App

A Flutter application built with **MVVM architecture** using **Provider** for state management and **Dependency Injection (DI)**.
It supports dynamic language switching and theming with persistent local storage using **SharedPreferences** and **unit/UI test cases**.

---

## ✨ Features

✅ MVVM Pattern with Provider
✅ Dependency Injection for clean architecture
🌐 Internationalization (English & Arabic)
🎨 Light & Dark Theme Support
💾 Local state persistence with SharedPreferences (theme & language)
🌍 Language Switcher UI
🔄 Code generation with `build_runner`
🌐 Generated i18n utils using `intl_utils`
**Test cases (unit, widget)** included


## 📁 Project Structure (MVVM)
lib/
├── core/                          # Core configuration: themes, localization, utils, and dependency injection
│   ├── style/                     # App-wide theme and styling
│   ├── translations/              # Generated and static localization files
│   ├── utils/                     # Utility classes and functions
│   └── di/                        # App-level dependency injection setup
│
├── features/
│   ├── news/
│   │   ├── data/                  # Remote API calls and repository implementations
│   │   ├── domain/                # Models and abstract repository contracts
│   │   ├── presentation/          # UI layer with notifiers, pages, and widgets
│   │   └── news_injections.dart   # News feature-specific DI setup
│   │
│   └── splash/                    # Splash screen logic and helper utilities
│
├── shared/                        # Reusable shared components across the app
│   ├── widgets/                   # Commonly used UI components (buttons, cards, etc.)
│   ├── pages/                     # Shared pages like webview, photo viewer
│   └── helpers/                   # Utility functions or classes shared app-wide


---

## 🚀 Getting Started

### 🔧 Prerequisites

- [Flutter SDK](https://docs.flutter.dev/get-started/install) (Version: 3.29.2)
- Dart SDK (comes with Flutter)
- Android Studio or VS Code (with Flutter & Dart plugins)

---

## 🛠️ Installation & Setup

### 1. Clone the repository
git clone https://github.com/hardikt1793/Kagi_News.git

### 2. Installation of the dependencies
flutter pub get

### 3. Generate localization and other generated files
`This step uses build_runner to generate necessary files like .g.dart and localization strings from intl_utils.`
- flutter pub run build_runner build --delete-conflicting-outputs
- dart run intl_utils:generate

### 4. Running app in device

* For running app in Android:
    * Go to project root and execute the following command in console to get the required dependencies:
        * flutter doctor
        * flutter pub get
    * Connect the device(Simulator/Physical) and allow installation
    * Run the project using the following command: flutter run

* For running app in iOS:
    * Go to project root and execute the following command in console to get the required dependencies:
        * flutter doctor
        * flutter pub get
        * cd ios
        * rm -rf ios/Pods ios/Podfile.lock
        * pod repo update
        * pod update
    * Connect the device(Simulator/Physical) and allow installation
    * Run the project using the following command: flutter run
