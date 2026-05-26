🇺🇸 **Read this in English** | 🇪🇸 [Leer en Español](README.md)

# 🇨🇴 FitBoxGo: Optimize Strength with Precision

**FitBoxGo** is the definitive tool for athletes seeking to eliminate guesswork in strength training. Designed to centralize progress, the application automates the most complex gym calculations to allow total focus on lifting.

---

### 🚀 Key Features

* **Intelligent 1RM Management:** Precise One-Repetition Maximum calculation based on current lifts.
* **Dynamic Plate Calculator:** Advanced algorithm that calculates the exact plate distribution based on the user's actual inventory (configuration via *checkboxes*).
* **Bidirectional Plate Calculator (Kg/Lb):** Exact indication of the plates needed for the barbell. Compatible with **Kilograms** and **Pounds**, adapting to any equipment.
* **Firebase Remote Config:** Remote control system to force version updates and deploy configurations in real-time.
* **WOD Benchmarks:** Performance tracking module for *Workouts of the Day* with level categorization (**RX, Intermediate, Scaled**) and support for time or repetition metrics.
* **Cloud Sync:** Event-driven architecture with Firestore for a consistent experience between Android and iOS.
> **FitBoxGo. Activate your best version.**

---
### 🎥 Demo: Feature Walkthrough

To facilitate immediate visualization of the user flow, I share these integrated short walkthroughs:

| Part 1: RM and Calculator | Part 2: Sync and WODs |
| :---: | :---: |
| ![Demo Part 1](https://github.com/user-attachments/assets/2c213f51-27bb-4f7c-a700-ae9629814a4e) | ![Demo Part 2](https://github.com/user-attachments/assets/38d15b9e-7900-4500-aa5c-b0e49c01e876) |


### 🛠️ Architecture and Tech Stack

#### **MVI (Model-View-Intent) Architecture**
Implementation of a unidirectional data flow to ensure a predictable and highly testable UI.

* **Data Layer:** Contains implementations of Firebase services (Authentication, Firestore/Storage, Remote Config).
* **Domain Layer:** Contains business logic, including the plate calculation engine and WOD validation rules.
* **Remote Config Integration:** Implementation of a reactive listener service that compares versions and triggers update alerts via native dialogs.
* **Design System:** Modular library in **Compose Multiplatform** that manages both the Dynamic Onboarding and theme adaptability (Light/Dark Mode).

To ensure that **FitBoxGo** is scalable and robust, a cutting-edge architecture has been implemented that separates business logic from the user interface.

---

### **Clean Architecture Diagram**

<img width="1536" height="1024" alt="Diagram_clean_architecture" src="https://github.com/user-attachments/assets/790f771d-2b35-4023-a362-6deb5a9ae911" />

---

### 🏗️ Multi-modular Structure

The application uses a modularized architecture to maximize reusability and maintainability:

* **`:domain` (The Core):** Pure business logic and calculation algorithms (RM, plates). 100% native Kotlin.
* **`:data`:** Data management. Includes `:service` (Firebase Cloud) and `:local` (Persistence).
* **`:features`:** Independent modules by functionality (Login, Dashboard, Records).
* **`:presentation`:** Reactive view logic under the MVI pattern.
* **`:design-system`:** Custom visual library in **Compose Multiplatform** for total consistency. Includes the dynamic onboarding engine.
* **`:navigation`:** Decoupled flow management between screens.
* **`:di`:** Centralized dependency injection with **Koin**.
* **`:app-android` / `:app-ios`:** Native entry points for each platform.

---

### 🛠️ Key Technologies

* **Compose Multiplatform (CMP):** 100% shared UI with native performance on Android and iOS.
* **Native Theme Support:** Dynamic detection of **Dark Mode / Light Mode** via the `:design-system`.
* **Kotlin Multiplatform (KMP):** Shared business logic and models.
* **Firebase Ecosystem:** Authentication (Google Login), Cloud Firestore (Real-time DB), and Remote Config.
* **Koin:** Lightweight DI optimized for multiplatform projects.
* **Coroutines and Flow:** Asynchronous reactivity engine for a fluid interface.

> *"Thanks to CMP, the design system maintains the tactile behavior and native performance of each operating system."*

---

### 🚀 Availability

**FitBoxGo** Focused on the fitness athlete community in **Colombia** 🇨🇴.

[![App Store](https://img.shields.io/badge/App_Store-Download-007AFF?style=for-the-badge&logo=apple&logoColor=white)](https://apps.apple.com/app/fitboxgo/id6761392693)

[![Google Play](https://img.shields.io/badge/Google_Play-Download-34A853?style=for-the-badge&logo=google-play&logoColor=white)](https://play.google.com/store/apps/details?id=org.javalenciab90.fitboxgo)

---

### ⚖️ Legal & Copyright
This repository is a **Technical Showcase**. The source code, design, and visual assets of **FitBoxGo** are the intellectual property of **Jaime Valencia**. Reproduction, distribution, or partial/total use of the material displayed is prohibited without prior authorization.

*© 2026 FitBoxGo. All rights reserved.*

---

### 📩 Contact

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/javalenciab90)
[![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/javalenciab90)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:javalenciab90@gmail.com)

**Jaime Valencia** *Mobile Software Developer | Android & Compose Multiplatform*
