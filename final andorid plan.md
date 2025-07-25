Here is a **comprehensive 90-hour training plan** for building the **SecureBank Android App** using **Kotlin + Jetpack Compose + Orbit MVI**, excluding Room DB, designed for intermediate Android developers.

---

## 🕘 **SecureBank Android App – 90 Hour Training Plan**

| **Phase**                          | **Module**               | **Topics Covered**                                                    | **Duration (hrs)** |
| ---------------------------------- | ------------------------ | --------------------------------------------------------------------- | ------------------ |
| 🟢 **Phase 1: Foundation & Setup** |                          |                                                                       |                    |
| 1                                  | Android App Architecture | MVVM vs MVI, Clean Architecture, Intro to Orbit MVI                   | 3                  |
| 2                                  | Project Setup & Tools    | Kotlin DSL, Hilt setup, Retrofit, Compose basics, folder structure    | 4                  |
| 3                                  | Git & CI/CD Basics       | GitHub Actions / CI pipelines for APK build, version control workflow | 2  (can be used for phase 4 /5 | 

| 🔹 **Subtotal**                    |                          | **9 hrs**                                                             |                    |

---

\| 🟦 **Phase 2: Orbit MVI Deep Dive**                      |                                                                                                             |                    |
\| 4         | Orbit MVI Fundamentals                      | ContainerHost, State, SideEffect, Intent, Unidirectional Data Flow                                          | 4                  |
\| 5         | Orbit in ViewModel + Compose UI Integration | Handling intents from UI, reacting to state and side effects                                                | 3                  |
\| 6         | Testing with Orbit                          | testContainer, state assertions, side effect tests                                                          | 2                  |
\| 🔹 **Subtotal**                                          |                                                                                                             | **9 hrs**          |

---

\| 🟨 **Phase 3: Authentication + State Management**        |                                                                                                             |                    |
\| 7         | Login Flow                                  | API integration, form validation, EncryptedSharedPreferences                                                | 4                  |
\| 8         | Token Storage + Logout                      | Auth token lifecycle, logout handling                                                                      | 2                  |
\| 9         | Orbit MVI in Auth Module                    | State management for login state/errors                                                                    | 2                  |
\| 🔹 **Subtotal**                                          |                                                                                                             | **8 hrs**          |

---

\| 🟧 **Phase 4: Dashboard, Transfer, Transactions**        |                                                                                                             |                    |
\| 10        | Dashboard Module                            | Display balance, cards, quick actions                                                                      | 3                  |
\| 11        | Fund Transfer UI + Validation               | Transfer screen, amount validation, success/fail dialog                                                    | 4                  |
\| 12        | Transaction List with Compose               | LazyColumn, filters, pull-to-refresh                                                                       | 3                  |
\| 13        | MVI for Transfer + Dashboard Modules        | Orbit state/event integration                                                                              | 3                  |
\| 🔹 **Subtotal**                                          |                                                                                                             | **13 hrs**         |

---

\| 🟨 **Phase 5: Bill Payment + Support Module**            |                                                                                                             |                    |
\| 14        | Bill Payment UI                             | Biller selection, input, payment confirmation                                                              | 3                  |
\| 15        | Support Ticketing                           | Raise/View tickets, status tracking                                                                        | 3                  |
\| 16        | MVI for Bills + Support                     | Integrating Orbit into these modules                                                                       | 2                  |
\| 🔹 **Subtotal**                                          |                                                                                                             | **8 hrs**          |

---

\| 🟪 **Phase 6: Settings + Accessibility + Offline**       |                                                                                                             |                    |
\| 17        | Settings Screen                             | Change PIN/password, biometric toggle, notification toggle                                                 | 3                  |
\| 18        | Accessibility Features                      | TalkBack, font scaling, semantic labeling                                                                  | 2                  |
\| 19        | Offline UI Mode                             | Show last synced state using SharedPreferences                                                             | 2                  |
\| 🔹 **Subtotal**                                          |                                                                                                             | **7 hrs**          |

---

\| 🔵 **Phase 7: Advanced Topics & Testing**                |                                                                                                             |                    |
\| 20        | Security Implementation                     | Input validation, secure logs, token safety                                                                | 2                  |
\| 21        | Testing Orbit ViewModels                    | Unit + MVI container tests                                                                                 | 3                  |
\| 22        | Compose UI Testing                          | `createComposeRule`, fake ViewModels                                                                       | 3                  |
\| 🔹 **Subtotal**                                          |                                                                                                             | **8 hrs**          |

---

\| 🟫 **Phase 8: API, DI, Utilities**                       |                                                                                                             |                    |
\| 23        | Retrofit + Moshi Setup                      | API config, error parsing                                                                                   | 2                  |
\| 24        | Repository + UseCases                       | Dependency inversion, usecase orchestration                                                                | 2                  |
\| 25        | Utility Classes & Extensions                | Validators, formatting helpers                                                                             | 2                  |
\| 🔹 **Subtotal**                                          |                                                                                                             | **6 hrs**          |

---

\| 🟩 **Phase 9: Finalization & Presentation**              |                                                                                                             |                    |
\| 26        | APK Build & Testing                         | Final testing + internal release                                                                           | 2                  |
\| 27        | Slide Preparation & Evaluation              | Training report, documentation, evaluation checklist                                                       | 2                  |
\| 28        | Final Demo & Q/A                            | Present working app, walkthrough, trainer feedback                                                         | 2                  |
\| 🔹 **Subtotal**                                          |                                                                                                             | **6 hrs**          |

---

### 🧮 **Total Duration: 90 Hours**

---

## 📋 Weekly Breakdown (Suggested)

| **Week** | **Topics**                                             | **Hours** |
| -------- | ------------------------------------------------------ | --------- |
| Week 1   | Phase 1 + Git + Orbit Intro                            | 12 hrs    |
| Week 2   | Orbit MVI + Auth Module                                | 12 hrs    |
| Week 3   | Dashboard + Transfer                                   | 12 hrs    |
| Week 4   | Transactions + Bill Payment + Support                  | 12 hrs    |
| Week 5   | Settings + Accessibility + Offline Support             | 10 hrs    |
| Week 6   | Testing + Security + API + DI                          | 12 hrs    |
| Week 7   | Finalization + APK + Slide + Evaluation + Presentation | 10 hrs    |

---


