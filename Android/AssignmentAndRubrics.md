📘 **Trainee Assignment Pack (Week-wise)** and 📊 **Final Project Evaluation Rubric** for the **SecureBank Android Banking App** training program.

---

# 🎓 Weekly Trainee Assignment Pack

| **Week**                                 | **Topics**                                                       | **Assignments**                                                                                                                                                    |
| ---------------------------------------- | ---------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Week 1**<br>*Intro + Kotlin Basics*    | - Android Studio Setup<br>- Kotlin Variables, Classes, Functions | ✅ Setup Android Studio & Emulator<br>✅ Create a basic Kotlin CLI app for ATM simulation<br>✅ Prepare ERD for Banking App                                           |
| **Week 2**<br>*Jetpack Compose UI*       | - Composables, Layouts, State                                    | ✅ Design Login Screen UI<br>✅ Design Home Dashboard UI with Balance & Quick Actions<br>✅ Implement state-driven Toggle for "Show Balance"                          |
| **Week 3**<br>*Navigation + Forms*       | - Navigation Component<br>- Input validation                     | ✅ Add navigation: Login → Home → Transfer<br>✅ Implement Fund Transfer Form with validations<br>✅ Handle backstack behavior manually                               |
| **Week 4**<br>*MVVM + Architecture*      | - ViewModel, Clean Arch layers                                   | ✅ Implement `DashboardViewModel` and `TransactionViewModel`<br>✅ Setup domain → usecase → repo architecture<br>✅ Write 2 UseCases: `GetBalance`, `GetTransactions` |
| **Week 5**<br>*Retrofit + API*           | - Retrofit, Moshi/Gson, Repo                                     | ✅ Connect to a mock `/api/balance` API<br>✅ Fetch and display transactions in LazyColumn<br>✅ Simulate 401 error handling for expired token                        |
| **Week 6**<br>*Room DB + Offline Mode*   | - DAO, Room Entity, Sync                                         | ✅ Setup Room for Transaction Entity<br>✅ Display transactions from Room when offline<br>✅ Sync via a button                                                        |
| **Week 7**<br>*Accessibility + Security* | - TalkBack, EncryptedStorage                                     | ✅ Add contentDescription to all interactive elements<br>✅ Store JWT token securely using `EncryptedSharedPreferences`<br>✅ Implement biometric authentication mock |
| **Week 8**<br>*WorkManager + Hilt*       | - Background jobs, DI                                            | ✅ Use WorkManager to sync `/transactions` every 6 hrs<br>✅ Integrate Hilt in 2 ViewModels<br>✅ Show notification when sync is done                                 |
| **Week 9**<br>*Testing*                  | - Unit, UI, Mocking                                              | ✅ Write unit test for `TransferFundsUseCase`<br>✅ Compose test for `DashboardScreen` using fake ViewModel<br>✅ Use MockWebServer to test `/api/balance`            |
| **Week 10**<br>*Final Integration*       | - Full feature merge, testing                                    | ✅ Final merge of all modules<br>✅ Test edge cases: no network, expired token, API errors<br>✅ Accessibility test with Android Accessibility Scanner                |

---

# 📊 Final Project Evaluation Rubric (Out of 100)

| **Criteria**                            | **Max Marks** | **Evaluation Points**                                    |
| --------------------------------------- | ------------- | -------------------------------------------------------- |
| 1. **Architecture & Clean Code**        | 20            | MVVM separation, reusable components, DI usage           |
| 2. **User Interface (Jetpack Compose)** | 15            | Responsive UI, animations, LazyColumn usage              |
| 3. **API Integration & Error Handling** | 15            | Proper Retrofit setup, error boundaries, retry logic     |
| 4. **Room + Offline Mode**              | 10            | Cached transactions, fallback UI, data consistency       |
| 5. **Security Practices**               | 10            | Encrypted token storage, biometric/auth simulation       |
| 6. **Accessibility Compliance**         | 10            | Proper labeling, content descriptions, font scaling      |
| 7. **Background Jobs + Notifications**  | 5             | Periodic sync, WorkManager, meaningful notifications     |
| 8. **Testing (Unit + UI)**              | 10            | ComposeTestRule usage, coverage for ViewModels/UseCases  |
| 9. **Project Packaging & Deployment**   | 5             | APK signing, proper Gradle config, working release build |
| **TOTAL**                               | **100**       |                                                          |

---

