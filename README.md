# Tip Calculator — Hybrid Android Application

A React-based Tip Calculator packaged as a Hybrid Android application using **Capacitor**. The project demonstrates how an existing web application can be adapted for Android without rewriting the frontend in native Kotlin.

## Features

- Calculate tips based on the bill amount and selected tip percentage.
- View the calculated tip and total bill.
- Use the application through a mobile-friendly interface.
- Run the React application in a web browser or as an Android application.

_The exact features depend on the functionality implemented in the original React application._

## Technology Stack

- **Frontend:** React, JavaScript, HTML, CSS
- **Hybrid Framework:** Capacitor 6
- **Android Platform:** Android Studio, Gradle
- **Package Management:** npm

## Project Structure

```text
tip-calculator-app/
├── public/                 # Static assets
├── src/                    # React application source
├── build/                  # Production web build
├── android/                # Native Android project
├── APK/
│   └── tip-calculator.apk   # Android APK
├── capacitor.config.*      # Capacitor configuration
├── package.json
└── README.md
```

## Run the Web Application

Install the project dependencies:

```bash
npm install
```

Start the development server:

```bash
npm start
```

To test the existing production build locally:

```bash
npx serve -s build
```

## Build the Android Application

Ensure Node.js, JDK 17, Android Studio and the Android SDK are installed.

Sync the web assets with the Android project:

```bash
npx cap sync android
```

Open the Android project:

```bash
npx cap open android
```

In Android Studio, select:

**Build → Build Bundle(s) / APK(s) → Build APK(s)**

The generated debug APK is typically located at:

```text
android/app/build/outputs/apk/debug/app-debug.apk
```

## Download the APK

The Android APK is available in the [`APK/`](APK/) directory.

Download `tip-calculator.apk`, transfer it to an Android device, and install it. Your device may ask you to allow installation from that source.

## Hybrid Application Architecture

The application uses React for its user interface and application logic. Capacitor packages the production web assets inside a native Android project, which runs the application through an Android WebView.

```text
React Web Application
         ↓
Production Build
         ↓
Capacitor
         ↓
Native Android Project
         ↓
      APK File
```

## Author

**Aryan Sethi**
