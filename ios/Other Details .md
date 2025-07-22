
---

# 📄 Case Study: SwiftBank – iOS Banking Application

## 1. 🧭 Objective

Develop a **secure**, **accessible**, and **responsive mobile banking app** using SwiftUI, MVVM + Clean Architecture, Combine, and Core Data with REST API integration.

---

## 2. 📌 Functional Requirements (FR)

| #   | Feature                  | Description                                    |
| --- | ------------------------ | ---------------------------------------------- |
| FR1 | **User Authentication**  | Secure login using username/password and token |
| FR2 | **Dashboard**            | Display account summary, balance, and actions  |
| FR3 | **Fund Transfer**        | Transfer to existing or new beneficiary        |
| FR4 | **Transaction History**  | View past transactions with filters            |
| FR5 | **Utility Bill Payment** | Simulated bill payments (electricity, gas)     |
| FR6 | **Support Ticketing**    | Submit and view service requests               |
| FR7 | **Offline Access**       | Show last synced data when API fails           |
| FR8 | **Logout**               | Token clear and local data wipe                |

---

## 3. 🔒 Non-Functional Requirements (NFR)

| #    | Requirement            | Details                                          |
| ---- | ---------------------- | ------------------------------------------------ |
| NFR1 | **Security**           | Keychain for token storage, no sensitive logging |
| NFR2 | **Performance**        | All operations under 500ms                       |
| NFR3 | **Clean Architecture** | Domain, Presentation, Data separation            |
| NFR4 | **Accessibility**      | VoiceOver, Dynamic Type, semantic traits         |
| NFR5 | **Testability**        | ≥ 80% test coverage                              |
| NFR6 | **Offline Mode**       | Core Data caching                                |
| NFR7 | **Background Sync**    | Combine-powered sync every 6 hours               |

---

## 4. 🧩 Architecture Overview

* **SwiftUI for UI**
* **Combine for reactivity**
* **URLSession for API**
* **Core Data for offline caching**
* **MVVM + Clean Architecture**:

  * `Presentation`: SwiftUI Views + ViewModels
  * `Domain`: UseCases, Entities
  * `Data`: API, Repository, Core Data

---

## 5. 🧪 Testing Scope

| Layer      | Tests                                 |
| ---------- | ------------------------------------- |
| UseCases   | Unit Tests (XCTest)                   |
| ViewModels | Mocked tests with published data      |
| Network    | Async/Await + Result type handling    |
| UI         | SwiftUI preview & Accessibility audit |

---

# 📘 Weekly Assignment Pack

| **Week**    | **Topic**                  | **Assignments**                                                                                                      |
| ----------- | -------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| **Week 1**  | Swift + Xcode Setup        | ✅ Install Xcode & create CLI ATM simulation<br>✅ Draw ERD for app<br>✅ Setup SwiftBank Xcode project                 |
| **Week 2**  | SwiftUI Basics             | ✅ Design Login & Dashboard Screens<br>✅ Add dummy balance state toggle with @State                                   |
| **Week 3**  | Navigation + Forms         | ✅ Navigation from Login → Home → Transfer<br>✅ Add Transfer Form with validation and alerts                          |
| **Week 4**  | MVVM + Clean Arch          | ✅ Create ViewModels: `DashboardViewModel`, `TransferViewModel`<br>✅ Implement 2 UseCases with mock data              |
| **Week 5**  | REST API Integration       | ✅ Connect to `/balance`, `/transactions` endpoints<br>✅ Parse JSON using `Codable` and show list                     |
| **Week 6**  | Core Data & Offline Mode   | ✅ Setup Core Data Entity for Transactions<br>✅ Show cached data if API fails                                         |
| **Week 7**  | Accessibility & Security   | ✅ Add accessibility labels to all forms<br>✅ Store JWT securely in Keychain<br>✅ Simulate TouchID/FaceID switch      |
| **Week 8**  | Combine + Background Tasks | ✅ Fetch `/transactions` using Combine<br>✅ Notify on successful background sync                                      |
| **Week 9**  | Testing                    | ✅ Write unit test for `TransferFundsUseCase`<br>✅ Compose UI test with fake ViewModel<br>✅ Async test for API result |
| **Week 10** | Final Delivery             | ✅ Polish UI<br>✅ Ensure all flows work offline<br>✅ Final demo with API, error cases, and accessibility testing      |

---

# 📊 Final Project Evaluation Rubric (100 Points)

| **Criterion**                          | **Weight** | **Details**                                           |
| -------------------------------------- | ---------- | ----------------------------------------------------- |
| ✅ **Architecture & Code Structure**    | 20         | MVVM & Clean layering, code reusability               |
| 🎨 **User Interface & UX**             | 15         | Use of SwiftUI, responsiveness, accessibility         |
| 🌐 **API Integration & Data Handling** | 15         | Proper REST integration, decoding, and error handling |
| 💾 **Core Data Offline Support**       | 10         | Caching transactions, fallback UI                     |
| 🔒 **Security Implementation**         | 10         | Keychain usage, secure logout, biometric auth         |
| 🔁 **Combine + Background Tasks**      | 10         | Reactive updates, periodic sync                       |
| 🧪 **Testing (Unit + UI)**             | 10         | UseCase + ViewModel + async tests                     |
| ♿ **Accessibility Compliance**         | 5          | VoiceOver, Dynamic Type, semantic tags                |
| 📦 **Project Packaging & Delivery**    | 5          | Clean repo, release-ready build                       |
| 🧑‍🏫 **Presentation & Demo**          | 5          | Clear walkthrough and flow demonstration              |

---

