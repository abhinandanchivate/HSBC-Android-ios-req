 **banking application-focused training session plan (60 hrs)** with **case-study based implementation** integrating:

* **Kotlin + Jetpack Compose**
* **Modern Android Architecture (MVVM + Clean)**
* **REST APIs (FastAPI/Node.js backend assumed)**
* **Security, Accessibility, Testing, and Performance**

---

## 🧠 Case Study Overview: **Mobile Banking App**

### Objective:

Design and develop a secure mobile banking app that allows users to:

* View account balance
* Transfer funds
* View transaction history
* Pay utility bills
* Raise service requests

---

## 📅 Training Plan with Case Study Mapping (60 Hours)

| **Week / Module**                | **Topics**                                                                                             | **Case Study Tasks / Projects**                                                                                          | **Hours** |
| -------------------------------- | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ | --------- |
| **1. Android + Kotlin Basics**   | - Android Studio Setup<br>- Kotlin Basics: variables, classes, null safety<br>- App Structure & Gradle | - Setup project for "Banking App"<br>- Splash/Login screen UI<br>- Kotlin models: User, Account, Transaction             | 8 hrs     |
| **2. Compose UI Fundamentals**   | - Composable Functions, State, Row/Column<br>- Navigation Components<br>- Input Fields & Buttons       | - Home screen UI: Balance + Menu<br>- Navigation setup: Login → Home → Transfer<br>- Forms: Fund Transfer, Bill Pay      | 8 hrs     |
| **3. MVVM + Clean Architecture** | - ViewModel, Repository Pattern<br>- Domain/Data/Presentation layers                                   | - Implement `AccountViewModel`, `TransactionRepo`<br>- Create use cases: `GetBalanceUseCase`, `TransferFundsUseCase`     | 6 hrs     |
| **4. REST API Integration**      | - Retrofit + Gson/Moshi<br>- API Layer Setup<br>- Error Handling                                       | - Connect to backend (e.g., `/api/balance`, `/api/transfer`)<br>- Show transaction history from REST response            | 6 hrs     |
| **5. Advanced Compose + State**  | - State Hoisting<br>- ViewModel Integration<br>- Dialogs & Alerts<br>- LazyColumn                      | - List of past transactions with filters<br>- Alert on failed transaction<br>- Dynamic data-driven UIs                   | 6 hrs     |
| **6. Room DB & Offline Sync**    | - Room Setup<br>- DAO, Entity, ViewModel Sync<br>- Integration with Retrofit                           | - Store cached transaction history<br>- Offline display of last known balance                                            | 4 hrs     |
| **7. Security & Accessibility**  | - EncryptedSharedPrefs<br>- TalkBack support<br>- contentDescription + Semantics                       | - Secure token storage<br>- Accessibility tagging for input fields and buttons                                           | 4 hrs     |
| **8. Background Jobs + DI**      | - WorkManager + CoroutineWorker<br>- Hilt for DI                                                       | - Background sync of transaction history every 6 hrs<br>- Inject `TransactionRepo` with Hilt                             | 4 hrs     |
| **9. Testing & CI Integration**  | - JUnit, Coroutine test utils, Compose Test APIs<br>- Mock APIs with Mockito or FakeServer             | - Write tests for `TransferFundsUseCase`<br>- Test `BalanceScreen` UI with composeTestRule                               | 4 hrs     |
| **10. Final Project Delivery**   | - End-to-End Implementation<br>- UI Polish + Animations<br>- Performance Optimizations                 | - Full deployment-ready APK<br>- App demo to simulate account use cases, including validations and success/failure flows | 4 hrs     |

---

## 📦 Key Modules & Case Study Implementation Mapping

| **App Module**          | **Technologies/Concepts**                               | **Screens/Features**                                     |
| ----------------------- | ------------------------------------------------------- | -------------------------------------------------------- |
| Authentication          | Jetpack Compose, Retrofit, ViewModel                    | Login Screen, Token Storage, Welcome Greeting            |
| Dashboard               | LazyColumn, ViewModel, Retrofit                         | Account Summary, Cards, Balance, Total Assets            |
| Fund Transfer           | Form UI, Validation, Retrofit + ViewModel               | Input receiver, amount → Transfer → Show Success/Failure |
| Transaction History     | LazyColumn, REST + Room                                 | List recent transactions with date/category filters      |
| Utility Bill Payment    | Dropdowns, Date Pickers, Input Forms                    | Select biller → Enter Amount → Confirm and Pay           |
| Support Tickets         | Compose Form, State Management                          | Raise issue → Ticket History with Status                 |
| Background Sync         | WorkManager + Retrofit                                  | Sync transaction data every 6 hours                      |
| Accessibility + Testing | Accessibility Scanner, composeTestRule, Mock ViewModels | Semantic labels, dynamic font sizes, test all flows      |

---

## 📁 Suggested Folder Structure (Clean Architecture)

```
com.bankapp
│
├── data
│   ├── api/ (Retrofit services)
│   ├── db/ (Room database)
│   ├── model/
│   └── repository/
│
├── domain
│   ├── model/
│   ├── usecase/
│
├── presentation
│   ├── ui/
│   │   ├── login/
│   │   ├── dashboard/
│   │   ├── transactions/
│   │   ├── transfer/
│   │   └── support/
│   └── viewmodel/
│
├── di/ (Hilt modules)
└── utils/
```

---

## ✅ Deliverables for Trainees

1. ✅ Fully working **Banking App** with Compose
2. ✅ Backend REST integration using mock server or FastAPI
3. ✅ Unit tests + UI tests + background sync
4. ✅ Secure & accessible Android app
5. ✅ Final ZIP + APK + Source Code (Git)
6. ✅ Presentation on Clean Architecture + Demo walkthrough

---


