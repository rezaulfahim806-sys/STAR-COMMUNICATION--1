# STAR COMMUNICATION — APK Build Guide

Prepared Android Studio project for the STAR COMMUNICATION ISP Admin app.

## Build debug APK
1. Open the `STAR_COMMUNICATION` folder in Android Studio.
2. Let Gradle sync/download the required components:
   - Android Gradle Plugin 8.6.1
   - Gradle 8.7
   - Android SDK Platform 35
   - Android SDK Build-Tools
3. Select **Build → Build APK(s)**.
4. APK output: `app/build/outputs/apk/debug/app-debug.apk`

## Project settings
- compileSdk: 35
- targetSdk: 35
- minSdk: 23
- applicationId: `com.starcommunication.isp`
- versionName: `1.0`

## Current features
- Dashboard with customer, paid/unpaid, income/expense and net balance
- Customer add/details/search/delete
- Monthly billing and payment history
- bKash incoming transaction queue with manual approval/cancel
- Server/API login and cloud refresh hooks
- OLT monitoring screen (demo ONU data) and OLT connection settings
- Android notifications for pending bKash transactions

## Important
The APK can connect to a backend API configured from Server Login/Settings. The current OLT screen is a UI/demo monitoring layer; real OLT/MikroTik communication still requires a backend integration. Keep bKash API credentials on the backend, not inside the APK.

Configured customer-payment bKash number: **01897-099850**. Incoming transactions remain pending until the admin manually confirms them; they are never auto-paid.
