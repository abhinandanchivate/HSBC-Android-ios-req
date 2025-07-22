 **comprehensive case study document** for the **Banking Mobile App Case Study**, aligned with your Android Development course and the training plan above.

---

# 📄 Case Study: **Mobile Banking Application**

## 1. 📌 Case Study Title

**SecureBank** – A modern Android-based mobile banking solution with accessibility, performance, and scalability at its core.

---

## 2. 🧭 Objective

To design and develop a real-time, secure, and responsive **Mobile Banking App** using **Kotlin, Jetpack Compose, MVVM Clean Architecture**, and **REST API integration**. The app supports user account management, fund transfers, bill payments, and more.

---

## 3. 🧱 Functional Requirements (FR)

| #    | Feature                    | Description                                                         |
| ---- | -------------------------- | ------------------------------------------------------------------- |
| FR1  | **User Authentication**    | Secure login using username/password and backend token verification |
| FR2  | **Dashboard**              | Display account summary, total balance, card limits                 |
| FR3  | **Fund Transfer**          | Transfer money to saved/new beneficiaries                           |
| FR4  | **Transaction History**    | View filtered transaction list (date range, type)                   |
| FR5  | **Utility Bill Payments**  | Pay electricity, water, gas, mobile bills                           |
| FR6  | **Raise Support Tickets**  | Submit and view complaints or service requests                      |
| FR7  | **Settings**               | Manage profile, change PIN, enable notifications                    |
| FR8  | **Offline Mode**           | Show last synced data when offline                                  |
| FR9  | **Accessibility Features** | TalkBack, dynamic font, semantic labeling                           |
| FR10 | **Logout**                 | Secure logout and clear local tokens/data                           |

---

## 4. 🛡️ Non-Functional Requirements (NFR)

| #    | Requirement              | Description                                                         |
| ---- | ------------------------ | ------------------------------------------------------------------- |
| NFR1 | **Security**             | Use EncryptedSharedPreferences, token-based auth, input validations |
| NFR2 | **Performance**          | All operations < 500ms with offline caching                         |
| NFR3 | **Scalability**          | Codebase ready for adding new features (e.g., loan section)         |
| NFR4 | **Maintainability**      | MVVM + Clean Architecture + modular code                            |
| NFR5 | **Accessibility**        | Must pass Android Accessibility Scanner                             |
| NFR6 | **Testing**              | ≥ 80% unit test coverage with Compose UI tests                      |
| NFR7 | **Battery Optimization** | Background jobs run efficiently (WorkManager constraints)           |

---

## 5. 📱 App Modules and Features Breakdown

### 5.1 Authentication Module

* Login screen with form validation
* Backend integration using Retrofit
* Secure token storage (EncryptedSharedPreferences)

### 5.2 Home/Dashboard Module

* Welcome user message
* Display of balance, accounts, credit cards, and quick actions

### 5.3 Transfer Module

* Add new payee or select from saved list
* Transfer screen with validation (amount limits, format)
* Success/failure dialogs

### 5.4 Transaction Module

* LazyColumn to display list of transactions
* Date range filter
* Pull-to-refresh and retry mechanism

### 5.5 Bill Payment Module

* Select biller (dropdown)
* Enter account/consumer number
* Show amount due and confirm payment

### 5.6 Support Ticket Module

* File new support request (dropdown + text input)
* Ticket history list with statuses

### 5.7 Settings Module

* Change password/PIN
* Toggle biometric login
* Enable/disable notifications

---

## 6. 🧩 Technical Architecture

### 6.1 Clean Architecture Layers

* **Presentation**: Jetpack Compose UIs, ViewModels
* **Domain**: UseCases, domain models (pure Kotlin)
* **Data**: Retrofit API, Room DB, Repositories

### 6.2 Jetpack Compose Usage

* Stateless/stateful composables
* State Hoisting
* Animations (fade, slide)
* LazyColumn, Dialog, Navigation Component

### 6.3 Modern Android Tools

| Tool               | Purpose              |
| ------------------ | -------------------- |
| Hilt               | Dependency Injection |
| Room               | Offline caching      |
| Retrofit + Moshi   | API integration      |
| WorkManager        | Background sync      |
| kotlinx.coroutines | Async flows          |
| Flow + LiveData    | Reactive UI          |

---

## 7. 🧪 Testing Strategy

| Layer       | Test Type              | Tools                                |
| ----------- | ---------------------- | ------------------------------------ |
| Domain      | Unit Test for UseCases | JUnit, Kotlin Test                   |
| Data        | Mock API & DAO tests   | Mockito, MockWebServer               |
| UI          | Compose UI Tests       | `createComposeRule`, fake ViewModels |
| Integration | Retrofit error tests   | MockServer                           |

---

## 8. 🔐 Security Measures

* HTTPS API endpoints
* Input validation (Kotlin extension functions)
* Secure local storage via `EncryptedSharedPreferences`
* Logout clears all sensitive local data
* No logs for sensitive info

---

## 9. 📶 Network Architecture

* Backend (FastAPI or Node.js)

  * `/api/login` – returns JWT
  * `/api/balance` – fetch account balance
  * `/api/transactions` – fetch transaction list
  * `/api/transfer` – post transfer data
  * `/api/bills` – bill types and history
  * `/api/support` – support tickets

---

## 10. 📂 Suggested Folder Structure

```
com.securebank
├── data/
│   ├── api/
│   ├── db/
│   ├── repository/
├── domain/
│   ├── model/
│   ├── usecase/
├── presentation/
│   ├── ui/ (per module)
│   └── viewmodel/
├── di/ (Hilt modules)
├── utils/
└── test/
```

---

## 11. 🚀 Final Project Milestones

| Milestone | Description                                   | Delivery Format    |
| --------- | --------------------------------------------- | ------------------ |
| M1        | App skeleton setup + Login + Navigation       | Git repo commit    |
| M2        | Dashboard + Fund Transfer screens             | UI preview/demo    |
| M3        | Transaction & Bill Module                     | Working API + DB   |
| M4        | Final Testing, Offline Support, Accessibility | APK + Report       |
| M5        | Final Presentation                            | Slides + Live Demo |

---

## 12. 📋 Evaluation Rubric (Trainer)

| Criteria                  | Max Score | Notes                        |
| ------------------------- | --------- | ---------------------------- |
| Code Quality & Clean Arch | 20        | Layer separation, modularity |
| UI & UX                   | 20        | Compose best practices       |
| REST API Integration      | 15        | Error handling, retry logic  |
| Offline Support           | 10        | Room + fallback UI           |
| Accessibility             | 10        | Tested with TalkBack         |
| Testing Coverage          | 15        | Unit & UI tests              |
| Security Handling         | 10        | Tokens, PIN, logout safety   |

---


