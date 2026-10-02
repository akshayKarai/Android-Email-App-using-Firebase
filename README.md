# Android Email App Using Firebase

An Android email-style application built with **Android and Google Firebase**. The project demonstrates user authentication, cloud-based data storage, inbox management, composing messages, replying to emails, and deleting messages.

## 📱 Project Overview

This project implements a simple email/messaging application for Android using **Firebase as the backend**.

Users can:

* Create an account and securely authenticate using Firebase
* Sign in to the application
* View their inbox
* Compose and send messages
* View individual messages
* Reply to specific recipients
* Delete messages
* Store and manage user and email data in Firebase

The project demonstrates how a mobile application can integrate with a cloud backend to provide authentication and persistent data storage without requiring a custom server.

---

## ✨ Features

### 🔐 User Authentication

Users can create accounts and authenticate through Firebase.

```text
User
 │
 ├── Sign Up
 │
 ▼
Firebase Authentication
 │
 └── User Account
```

Firebase is used to manage authentication and user account information.

### 📥 Inbox

Users can view messages received in their inbox.

```text
┌───────────────────────────┐
│          Inbox            │
├───────────────────────────┤
│ From: user@example.com    │
│ Subject: Hello            │
├───────────────────────────┤
│ From: another@example.com │
│ Subject: Meeting          │
└───────────────────────────┘
```

### ✉️ Compose Message

Users can create and send a new email/message by providing the recipient and message content.

### ↩️ Reply

Users can open an existing message and reply directly to the recipient.

### 🗑️ Delete Messages

Users can delete messages from their inbox, with the corresponding data removed from Firebase.

### ☁️ Firebase Integration

Firebase provides the cloud backend for:

* Authentication
* User data
* Email/message data
* Persistent cloud storage

---

# 🏗️ Application Architecture

The overall application flow can be represented as:

```text
                 ┌───────────────────┐
                 │   Android App     │
                 └─────────┬─────────┘
                           │
             ┌─────────────┼─────────────┐
             │             │             │
             ▼             ▼             ▼
        Authentication   Inbox       Compose
             │             │             │
             └─────────────┼─────────────┘
                           │
                           ▼
                 ┌───────────────────┐
                 │      Firebase     │
                 │      Backend      │
                 └─────────┬─────────┘
                           │
              ┌────────────┴────────────┐
              │                         │
              ▼                         ▼
       Authentication              Database
```

---

# 🛠️ Technologies Used

| Technology                  | Purpose                                  |
| --------------------------- | ---------------------------------------- |
| **Java / Android**          | Mobile application development           |
| **Android SDK**             | Android application framework            |
| **Firebase Authentication** | User registration and authentication     |
| **Firebase Database**       | Cloud-based storage for application data |
| **Android Studio**          | Development environment                  |

> **Note:** This repository was originally created several years ago. Android Studio, Gradle, Firebase SDKs, and Android APIs have evolved significantly since then. The project may require dependency and configuration updates before building with a current Android development environment.

---

# 📂 Project Screens

The repository includes screenshots demonstrating the primary application screens.

### Main Screen

The main application screen provides access to the application's core functionality.

<img src="https://github.com/akshayKarai/Android-Email-App-using-Firebase/blob/master/Main%20Screen.png?raw=true" width="300">

---

### Sign Up Screen

The sign-up screen allows new users to create an account.

<img src="https://github.com/akshayKarai/Android-Email-App-using-Firebase/blob/master/SignUp%20Screen.png?raw=true" width="300">

---

### Inbox

The inbox displays messages associated with the authenticated user.

<img src="https://github.com/akshayKarai/Android-Email-App-using-Firebase/blob/master/Inbox.png?raw=true" width="300">

---

### Compose Screen

Users can compose and send new messages.

<img src="https://github.com/akshayKarai/Android-Email-App-using-Firebase/blob/master/Compose%20Screen.png?raw=true" width="300">


---

# 🔄 Application Workflow

The application follows a straightforward email workflow.

```text
                    ┌───────────────┐
                    │     Start     │
                    └───────┬───────┘
                            │
                            ▼
                    ┌───────────────┐
                    │ Authentication│
                    └───────┬───────┘
                            │
                 ┌──────────┴──────────┐
                 │                     │
              New User             Existing User
                 │                     │
                 ▼                     ▼
              Sign Up                Sign In
                 │                     │
                 └──────────┬──────────┘
                            │
                            ▼
                    ┌───────────────┐
                    │  Main Screen  │
                    └───────┬───────┘
                            │
             ┌──────────────┼──────────────┐
             │              │              │
             ▼              ▼              ▼
           Inbox         Compose         Other
             │              │
             ▼              ▼
          Message          Send
             │
        ┌────┴────┐
        │         │
        ▼         ▼
      Reply     Delete
```

---

# 🔐 Firebase Integration

Firebase acts as the backend for the application.

### Authentication

The application uses Firebase Authentication to manage user accounts.

```text
Android Application
        │
        │ Sign Up / Sign In
        ▼
Firebase Authentication
        │
        ▼
Authenticated User
```

### Database

Application data is stored in Firebase and associated with users.

A conceptual structure can be represented as:

```text
Firebase
│
├── Users
│   ├── User 1
│   ├── User 2
│   └── User 3
│
└── Messages
    ├── Inbox
    ├── Sent Messages
    └── Message Data
```

The exact database structure depends on the Firebase configuration used by the original application.

---

# 📋 Core Functionality

| Functionality       | Description                              |
| ------------------- | ---------------------------------------- |
| User Registration   | Creates a new application account        |
| User Authentication | Authenticates registered users           |
| Inbox               | Displays received messages               |
| Compose             | Creates a new message                    |
| Send                | Sends and stores a message               |
| View Message        | Opens an individual message              |
| Reply               | Responds to an existing message          |
| Delete              | Removes a message                        |
| Cloud Storage       | Persists application data using Firebase |

---

# 🚀 Getting Started

Because this project was developed several years ago, additional configuration may be required to run it with a modern Android development environment.

## Prerequisites

* Android Studio
* Android SDK
* Java/JDK compatible with the project's Gradle configuration
* A Firebase project
* Android emulator or physical Android device

## 1. Clone the Repository

```bash
git clone https://github.com/akshayKarai/Android-Email-App-using-Firebase.git
```

Navigate into the project:

```bash
cd Android-Email-App-using-Firebase
```

## 2. Open in Android Studio

Open the project directory in Android Studio.

Allow Android Studio to synchronize the Gradle configuration.

> If the project uses an older Gradle or Android Gradle Plugin version, Android Studio may require compatibility updates before the project can be built.

## 3. Configure Firebase

Create or select a Firebase project and configure the Android application.

The Firebase configuration file should be added according to the Firebase Android setup instructions.

> Do not commit private credentials, API keys with inappropriate restrictions, service-account keys, or other sensitive Firebase configuration to a public repository.

## 4. Build the Application

After configuring the project and Firebase:

```text
Build → Make Project
```

or use the Gradle build system from the command line.

## 5. Run the Application

Connect an Android device or start an Android emulator and run the application from Android Studio.

---

# 📦 Repository Contents

The repository contains the following primary artifacts:

```text
Android-Email-App-using-Firebase/
│
├── Compose Screen.png
├── Inbox.png
├── Main Screen.png
├── SignUp Screen.png
├── Message me app.zip
└── README.md
```

The `Message me app.zip` archive contains the original application project files.

---

# 📸 Screenshots

| Screen      | Preview                         |
| ----------- | ------------------------------- |
| Main Screen | Application landing/main screen |
| Sign Up     | User registration               |
| Inbox       | Received messages               |
| Compose     | Create and send messages        |

The individual screenshots are available in the repository:

### Main Screen

<img src="https://github.com/akshayKarai/Android-Email-App-using-Firebase/blob/master/Main%20Screen.png?raw=true" width="300">

### Sign Up Screen

<img src="https://github.com/akshayKarai/Android-Email-App-using-Firebase/blob/master/SignUp%20Screen.png?raw=true" width="300">

### Inbox

<img src="https://github.com/akshayKarai/Android-Email-App-using-Firebase/blob/master/Inbox.png?raw=true" width="300">

### Compose Screen

<img src="https://github.com/akshayKarai/Android-Email-App-using-Firebase/blob/master/Compose%20Screen.png?raw=true" width="300">



---

# 🎯 Learning Objectives

This project demonstrates practical experience with:

* Android application development
* Firebase integration
* Firebase Authentication
* Cloud database integration
* User registration and authentication
* CRUD-style message operations
* Mobile UI development
* Cloud-backed application architecture
* Managing application data for authenticated users

---

# 📚 References

* [Android Developers](https://developer.android.com/)
* [Firebase Documentation](https://firebase.google.com/docs)
* [Firebase Authentication](https://firebase.google.com/docs/auth)
* [Firebase Documentation for Android](https://firebase.google.com/docs/android/setup)

---

# 📌 Project Status

This is an **academic/learning project** originally developed several years ago to demonstrate Android development and Firebase integration.

The project represents the technologies and implementation practices used at the time of development. Modernizing it would likely involve updating Android dependencies, Gradle configuration, Firebase SDKs, authentication configuration, and potentially the database implementation.

---

## 👨‍💻 Project Summary

**Android Email App Using Firebase** is a cloud-connected Android application that demonstrates how Firebase can be used as a backend for authentication and email-style messaging functionality.

The project provides a practical example of integrating a mobile frontend with cloud authentication and persistent data storage.
