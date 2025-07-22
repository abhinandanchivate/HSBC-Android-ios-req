Based on the uploaded **iOS syllabus (SwiftUI – 60 hrs)**, here is a complete **training session plan with a case study-based implementation** of a **Banking Application** for iOS using SwiftUI, Combine, Async/Await, and Clean Architecture.

---

## 📄 Case Study Title

**SwiftBank** – A modern, secure, and accessible iOS mobile banking app built using SwiftUI and Clean Architecture principles.

---

## 📅 iOS Banking App Training Plan (60 Hours)

| **Week**    | **Module**                     | **Topics**                                                                                   | **Case Study Tasks**                                                                                    | **Hours** |
| ----------- | ------------------------------ | -------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | --------- |
| **Week 1**  | Swift & Xcode Setup            | - Xcode Setup, Simulators<br>- Swift Syntax: vars, funcs, structs<br>- SwiftUI App Structure | ✅ Create ERD + Feature Mapping<br>✅ Swift CLI ATM Simulation<br>✅ Setup SwiftBank Project               | 8 hrs     |
| **Week 2**  | SwiftUI Basics                 | - Views, Modifiers, State<br>- VStack, HStack, ZStack<br>- NavigationView                    | ✅ Design Login Screen & Dashboard<br>✅ Create basic navigation flow: Login → Home → Profile             | 8 hrs     |
| **Week 3**  | Navigation + Forms             | - NavigationLink<br>- Forms, TextFields, Buttons<br>- @State and form validation             | ✅ Implement Fund Transfer UI<br>✅ Add input validations<br>✅ Success & failure alerts                   | 6 hrs     |
| **Week 4**  | MVVM + Clean Arch              | - ObservableObject, @Published<br>- Clean separation: Presentation / Domain / Data           | ✅ Create `DashboardViewModel` & `TransferViewModel`<br>✅ Define UseCases: `GetBalance`, `TransferFunds` | 6 hrs     |
| **Week 5**  | REST API Integration           | - URLSession + Codable<br>- Error handling, retry logic                                      | ✅ Integrate `/api/balance`, `/api/transactions`<br>✅ Show transaction list with error fallback          | 6 hrs     |
| **Week 6**  | Core Data & Caching            | - Core Data Setup<br>- Entity, FetchRequest, persistence                                     | ✅ Cache transactions locally<br>✅ Show offline mode UI when API fails                                   | 4 hrs     |
| **Week 7**  | Accessibility & Secure Storage | - VoiceOver, Dynamic Type<br>- Keychain for token storage                                    | ✅ Add accessibility labels<br>✅ Store auth token in Keychain<br>✅ Simulate BiometricAuth                | 4 hrs     |
| **Week 8**  | Combine + Background Tasks     | - Combine pipelines<br>- Background Fetch, Notifications                                     | ✅ Periodic sync using Combine<br>✅ Notify user when background sync is complete                         | 4 hrs     |
| **Week 9**  | Unit Testing                   | - XCTest<br>- Mocking ViewModels & API                                                       | ✅ Unit test use cases and ViewModels<br>✅ Test async/await functions<br>✅ SwiftUI snapshot preview test | 4 hrs     |
| **Week 10** | Final Project Integration      | - Feature integration<br>- Testing, Optimization                                             | ✅ Package app<br>✅ Present working flows (Login, Transfer, History)<br>✅ Final Demo & Code Review       | 4 hrs     |

---

## 📦 iOS Project Features & Architecture

### Key Functionalities

* ✅ Login and logout
* ✅ View balance and recent transactions
* ✅ Transfer funds (new or saved payees)
* ✅ Utility bill payment (simulated)
* ✅ Raise and track support tickets
* ✅ Offline transaction view

### Architecture (Clean)

* **Presentation Layer**: SwiftUI Views + ViewModels (ObservableObject)
* **Domain Layer**: Business UseCases (pure Swift)
* **Data Layer**: API Service (URLSession), Core Data, Repositories

---

## 📁 Suggested Folder Structure

```
com.swiftbank
├── Data
│   ├── API
│   ├── Repository
│   ├── CoreData
├── Domain
│   ├── Model
│   ├── UseCase
├── Presentation
│   ├── Screens (Dashboard, Transfer, etc.)
│   ├── ViewModels
├── Resources
│   └── Assets.xcassets, Localization
└── Utilities
    └── Network, Constants, Extensions
```

---

