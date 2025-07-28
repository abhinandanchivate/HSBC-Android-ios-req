 **90-hour iOS Banking App Training Plan** for the **SwiftBank** case study.



---

## 📄 Case Study Title

**SwiftBank** – A secure, modular mobile banking application using **SwiftUI + UIKit**, **TCA**, and **Clean Architecture**.

---

## 📅 Updated iOS Banking App Training Plan (90 Hours)

| **Week**    | **Module**                          | **Topics Covered**                                                                                         | **Case Study Tasks**                                                                                     | **Hours** |
| ----------- | ----------------------------------- | ---------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | --------- |
| **Week 1**  | Swift Basics + Project Setup        | - Swift fundamentals<br>- Xcode config<br>- SwiftUI & UIKit intro<br>- CLI banking sim                     | ✅ ERD & Flow Mapping<br>✅ Swift CLI ATM simulation<br>✅ SwiftBank Base Project Setup                     | 8 hrs     |
| **Week 2**  | UIKit vs SwiftUI + Navigation       | - SwiftUI Views, Stacks<br>- UIKit basics: UIViewController, Segues<br>- SwiftUI ↔ UIKit bridging          | ✅ Build Login (SwiftUI) & Profile (UIKit)<br>✅ Flow: Login → Home → Profile                              | 8 hrs     |
| **Week 3**  | Forms & Validations                 | - SwiftUI Form, TextFields, Alert<br>- UIKit TextField handling<br>- Error binding in views                | ✅ Create Fund Transfer screen (UIKit)<br>✅ Add validation and error alerts                               | 6 hrs     |
| **Week 4**  | MVVM to TCA Migration Basics        | - ObservableObject vs Store<br>- TCA Core Concepts: State, Action, Reducer<br>- Intro to `ReducerProtocol` | ✅ Setup AppState, Action, Reducer<br>✅ Migrate Login module to TCA                                       | 6 hrs     |
| **Week 5**  | Advanced TCA Structure              | - `Store`, `Reducer`, `Environment`<br>- Dependency Injection<br>- Binding ViewState to Store              | ✅ Create `DashboardFeature` with TCA<br>✅ Define Environment with APIClient                              | 6 hrs     |
| **Week 6**  | Modular Architecture with TCA       | - FeatureReducers<br>- NavigationStackStore<br>- State isolation                                           | ✅ Break down `TransferFeature`, `TransactionListFeature`<br>✅ Integrate via NavigationStack              | 6 hrs     |
| **Week 7**  | Async/Await + API Handling          | - `Effect.run`, `Effect.task`, `Dependencies`<br>- Async API call with TCA Effects                         | ✅ Add `/balance`, `/transfer`, `/transactions` endpoints<br>✅ Load on appear + reducer action dispatch   | 6 hrs     |
| **Week 8**  | TCA Middleware Equivalents          | - Side effects handling in TCA<br>- Combine + TCA Interop<br>- Debugging with `.print()`                   | ✅ Add logging effects<br>✅ Show API errors as `.alert` in reducer                                        | 6 hrs     |
| **Week 9**  | UIKit Integration with TCA          | - UIKit with `StoreViewController`<br>- TCA in UIKit screens                                               | ✅ Port Profile screen to UIKit with TCA<br>✅ Share global state between SwiftUI and UIKit via root store | 6 hrs     |
| **Week 10** | Keychain + Biometric Auth           | - SwiftKeychainWrapper<br>- BiometricAuth API<br>- Inject auth service into TCA environment                | ✅ Auth token via Keychain<br>✅ Face ID login screen<br>✅ Update state using TCA                          | 6 hrs     |
| **Week 11** | Combine & Background Fetch          | - Combine pipeline<br>- Background refresh<br>- NotificationCenter                                         | ✅ Background sync with Combine publisher<br>✅ Update state in reducer on completion                      | 6 hrs     |
| **Week 12** | State Persistence (optional / mock) | - Simulated memory-only state<br>- Rehydration techniques (via APIs)<br>- Secure token handling            | ✅ Show fallback UI when offline<br>✅ Simulate logout/token expiry flows                                  | 4 hrs     |
| **Week 13** | Testing in TCA                      | - Unit testing reducers<br>- Snapshot testing<br>- Dependency mocking                                      | ✅ Unit test transfer reducer<br>✅ Mock API client<br>✅ UI snapshot for dashboard                         | 6 hrs     |
| **Week 14** | Feature Integration & Refactoring   | - Folder restructuring<br>- Code cleanup<br>- Final polish                                                 | ✅ Finalize all modules<br>✅ Re-test flows (Login, Transfer, History)                                     | 6 hrs     |
| **Week 15** | Final Demo + Review                 | - Group walkthrough<br>- Demo all flows<br>- Feedback and handoff                                          | ✅ Final Presentation<br>✅ Code Review<br>✅ Optional App Store mock upload                                | 4 hrs     |

---

## ✅ Core App Features

| ✅ Features                     | 🧩 Architecture via TCA                      |
| ------------------------------ | -------------------------------------------- |
| Login/logout                   | `LoginFeature.State`, `LoginFeature.Reducer` |
| Transfer funds                 | `TransferFeature.State`, async effects       |
| Transaction history            | `TransactionListFeature`, API fetch          |
| Support ticket simulation      | Optional `SupportFeature`                    |
| Secure token & biometric login | Keychain + injected environment auth         |
| Background sync + notification | Combine-based background effect              |

---

## 🏛️ Clean + TCA Architecture Breakdown

| Layer            | Description                                                     |
| ---------------- | --------------------------------------------------------------- |
| **Presentation** | SwiftUI/UIViewController (calls `.send(action)` on `Store`)     |
| **Feature**      | TCA-based modules: State, Reducer, Action, View                 |
| **Domain**       | UseCases abstracted as environment dependencies                 |
| **Data Layer**   | APIService as `DependencyKey` injected into environment         |
| **Auth Layer**   | KeychainManager used in `AuthService`, injected via Environment |

---

## 📂 Folder Structure (TCA Best Practice)

```
com.swiftbank
├── App
│   ├── SwiftBankApp.swift
│   └── AppFeature.swift
├── Features
│   ├── LoginFeature/
│   ├── DashboardFeature/
│   ├── TransferFeature/
│   ├── TransactionListFeature/
│   └── ProfileFeature/ (UIKit)
├── UIKit
│   └── ProfileViewController.swift
├── Environment
│   ├── APIClient.swift
│   ├── AuthService.swift
│   └── AppDependencies.swift
├── Models
│   └── Transaction.swift, User.swift
├── Resources
│   └── Assets.xcassets, Localizable.strings
├── Tests
│   ├── ReducerTests/
│   ├── ViewTests/
│   └── IntegrationTests/
└── Utilities
    └── KeychainWrapper.swift, Constants.swift
```

---

## 🔁 State & Action Sample (TCA Style)

```swift
struct TransferFeature: Reducer {
  struct State: Equatable {
    var amount = ""
    var isTransferring = false
    var alert: AlertState<Action>?
  }

  enum Action {
    case amountChanged(String)
    case transferTapped
    case transferResponse(Result<Void, TransferError>)
    case alertDismissed
  }

  @Dependency(\.apiClient) var apiClient

  func reduce(into state: inout State, action: Action) -> Effect<Action> {
    switch action {
    case let .amountChanged(value):
      state.amount = value
      return .none

    case .transferTapped:
      state.isTransferring = true
      return .run { [amount = state.amount] send in
        let result = try await apiClient.transfer(amount: amount)
        await send(.transferResponse(result))
      }

    case let .transferResponse(.success):
      state.isTransferring = false
      return .none

    case let .transferResponse(.failure(error)):
      state.isTransferring = false
      state.alert = .init(title: TextState("Transfer Failed"))
      return .none

    case .alertDismissed:
      state.alert = nil
      return .none
    }
  }
}
```


