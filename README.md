# Android Sign-Up UI & Activity Navigation

An interactive, Material Design-based Sign-Up User Interface for Android. This project was developed as a core practical assignment for the Mobile Application Development course (IT 332). It demonstrates key Android engineering principles, including XML layout design, client-side input validation, and Activity lifecycle navigation using explicit Intents.

---

## 🚀 Key Features

*   **Material Design Forms:** Modern UI with outlined input text fields, 12dp rounded borders, and floating hint labels using `TextInputLayout`.
*   **Secure Password Input:** Integrated eye-toggle icons for password masking and visibility toggling.
*   **Keyboard Optimization:** Context-aware virtual keyboard setups (e.g., specific layouts for emails and passwords) for a seamless user experience.
*   **Responsive Layout:** Fully scrollable UI using `ScrollView` with `fillViewport` to prevent content clipping when the soft keyboard is open.
*   **Client-Side Validation:** Java-based input verification ensuring data integrity before form submission.
*   **Activity Navigation:** Smooth transitions between the Sign-Up screen (`MainActivity`) and the Welcome Dashboard (`HomeActivity`) using explicit Intents, with proper session termination (`finish()`).

## 🛠️ Tech Stack

*   **IDE:** Android Studio
*   **Language:** Java
*   **UI/Layout:** XML (Material Design Components)

## 📁 Project Structure

The project follows a standard Model-View-Controller (MVC) architecture, separating UI design (XML) from application logic (Java).

```text
app/
├── manifests/
│   └── AndroidManifest.xml             # Central manifest registering activities
├── kotlin+java/
│   └── com.example.signupuipage/       
│       ├── MainActivity.java           # Controller: Form Validation & Registration
│       └── HomeActivity.java           # Controller: Welcome Dashboard
└── res/
    └── layout/                         
        ├── activity_main.xml           # View: Sign-Up UI Layout
        └── activity_home.xml           # View: Welcome Dashboard Layout
```

## ⚙️ How to Run the Project

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/yourusername/your-repo-name.git
    ```
2.  **Open in Android Studio:**
    *   Launch Android Studio and select **Open**.
    *   Navigate to the cloned repository folder and select it.
3.  **Sync Gradle:** Wait for Android Studio to index the files and sync the Gradle project.
4.  **Run the App:**
    *   Select an Android Virtual Device (AVD) or connect a physical Android device.
    *   Click the green **Run** button (`Shift + F10`) in the top toolbar.

## 🎨 UI Design & Validation Logic

### UI Specifications
*   **Container:** `ScrollView` allows smooth vertical scrolling.
*   **Text Inputs:** `TextInputLayout` & `TextInputEditText` handle floating labels, error states, and password toggles.
*   **Buttons:** `MaterialButton` is used for the primary call-to-action (Sign Up) and secondary actions (Google Sign-In placeholder).

### Validation Rules (MainActivity.java)
Data integrity is verified before allowing navigation:
*   **Full Name:** Cannot be empty.
*   **Email Address:** Cannot be empty; must match valid email syntax (`Patterns.EMAIL_ADDRESS`).
*   **Password:** Minimum of 6 characters required.
*   **Confirm Password:** Must exactly match the original password field.

## 🔮 Future Scope

To elevate this project to production readiness, the following enhancements are planned:
*   **Firebase Authentication:** Replace local validations with a live backend using Firebase Auth and Google Identity Services SDK.
*   **Session Persistence:** Utilize Android's `EncryptedSharedPreferences` or Room Database to maintain user sessions across app restarts.
*   **Intent Data Passing:** Pass the verified 'Full Name' from `MainActivity` to `HomeActivity` via Intent extras to display a personalized greeting.
*   **Motion & Transitions:** Introduce Lottie vector animations and Shared Element Transitions for a polished UX.

---

**📄 Note:** For a comprehensive breakdown of the project architecture, UI matrices, and troubleshooting guides, please refer to the full documentation provided in the repository: [`4747_SignUp_Documentation.pdf`](./4747_SignUp_Documentation.pdf).
