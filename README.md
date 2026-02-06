# University Companion App 🎓📱

An educational Android application built with **Kotlin** and **Jetpack Compose**. The primary goal of this project is to simulate a simple university companion app that displays a course schedule and educational resources, with a core focus on **correct application architecture (MVVM + Repository Pattern)** rather than just UI aesthetics.

The app is developed as a crucial training phase for understanding robust data handling before integrating with real-world APIs. Data is sourced by reading a local JSON file within the app's `assets` folder.

## Key Technologies and Architectural Concepts 🛠️

The application is built using a modern Android stack:

-   **Kotlin:** The primary programming language.
-   **Jetpack Compose:** For building native, declarative user interfaces.
-   **MVVM Architecture:** **(Model-View-ViewModel)** for clean separation between UI and business logic.
-   **Repository Pattern:** For managing all data sources (local JSON simulation).
-   **Gson:** Used for converting JSON data streams into Kotlin Data Classes (Serialization/Deserialization).
-   **State Management:** Managed robustly via **ViewModel** (StateFlow) and **Compose State**.
-   **Android Intents:** Used for handling external actions like opening web links in the device's browser.

## Application Structure (Architecture Deep Dive) 🧱

The architecture adheres strictly to the principles of separation of concerns:

-   The **UI (Screens)** only interacts with the **ViewModel**.
-   The **ViewModel** is responsible for managing the UI State and requesting data.
-   The **Repository** is the single source of truth for fetching data.
-   **Data Flow:** Data is read from a local JSON file within the `assets` folder, simulating a network call.

This layered structure ensures:
-   **Testability:** Logic is easy to test independently of the UI.
-   **Scalability:** The architecture easily supports adding new features and data sources.
-   **Maintainability:** Clear and explicit code, making future development easier.
-   **Source Swapping:** The data source (Local JSON) can be swapped for a real API (**Retrofit**) without modifying the ViewModel or the UI (which is the main goal of the next phase).

## Application Screens 📸

### Home Screen
A simple, central hub for navigation between the app's main features.

### Schedule Screen
Displays the weekly course schedule, efficiently rendered using **LazyColumn** with data streamed from the ViewModel.

### Resources Screen
Displays educational resource links, which open in the device's web browser upon interaction using **Android Intents**.

## Project Goal (The Why) 🎯

This project serves as a key educational milestone to solidify my understanding of:
-   How data flows through a modern Android application (Data Flow).
-   How to correctly separate responsibilities (Separation of Concerns).
-   **The essential preparation for integrating real APIs and `Retrofit` in the next phase of this challenge.**

This project is a dedicated step in a professional Android development learning journey.

***<img width="120" height="240" alt="Screenshot_20260206_221310" src="https://github.com/user-attachments/assets/009b41f1-b17d-489c-9139-278d18c783fe" />
<img width="120" height="240" alt="Screenshot_20260206_221255" src="https://github.com/user-attachments/assets/2bf54b66-8adc-4638-8eda-daaf4f7190ea" />
<img width="120" height="240" alt="Screenshot_20260206_221234" src="https://github.com/user-attachments/assets/7c0a3615-31ac-4aa6-ab18-e243868ac117" />
