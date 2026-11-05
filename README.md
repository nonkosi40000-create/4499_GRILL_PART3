# 4499GRILL - Premium Wood-Fired Experience

4499GRILL is a cutting-edge Android application designed for a premium wood-fired grill restaurant. It goes beyond traditional food ordering by combining social community features, AI-driven recommendations, real-time order updates, multilingual accessibility, and secure cloud integration.

## 🚀 Key Features & Deep Dive

### 1. Smart Authentication & Role Management
The app features Firebase-backed authentication and **Single Sign-On (SSO)**, alongside support for multiple user roles:
*   **Customers:** Access to ordering, community, and personal history.
*   **Workers & Managers:** Specialized interfaces for order processing and restaurant oversight.
*   **Role-based routing:** After sign-in, users are routed to the appropriate dashboard according to their verified role in Firestore.

### 2. Intelligent Menu & Customization
*   **Dynamic Discovery:** High-performance menu rendering using Glide for image caching.
*   **Precision Customization:** The `ItemDetailActivity` supports required selections (such as patty type) and optional add-ons, recalculating totals as users customize their meals.

### 3. AI-Powered, Multilingual Concierge
*   **Personalized recommendations:** The integrated AI chat assistant suggests meals based on users' cravings and preferences.
*   **Chat in your language:** The chatbot supports **English, Afrikaans, and isiZulu**, allowing users to interact with the assistant in their selected language.
*   **Works within the chatbot:** The multilingual experience is applied not only to the app interface but also to the recommendation and conversation flow within the chatbot.

### 4. Community Hub (Social Dining)
*   **Social Interaction:** A social feed where users can post their meals, rate dishes with a 5-star system, and leave comments.
*   **Social Proof:** Like counters and community ratings help users discover popular dishes.

### 5. Advanced Order & Payment System
*   **Multi-Select Payments:** The `OrdersActivity` allows users to view their order history and select multiple "Awaiting Payment" orders to pay concurrently.
*   **Live Tracking:** Firestore snapshot listeners keep order status updates (Received -> Grilling -> Delivered) in sync without requiring a manual refresh.

### 6. Personalization, Language & Accessibility
*   **Multilingual interface:** The app supports **English, Afrikaans, and isiZulu**. Users can use the app and chatbot in their preferred supported language.
*   **Theme Control:** Dark Mode and Light Mode are available through the Profile settings. The preference is saved across app launches using SharedPreferences.

### 7. Firebase Blob Storage
*   **Media storage:** Firebase Storage is used as blob/object storage for app media, including food imagery and user-uploaded community content.

### 8. Automated Testing
*   **Validation:** Automated tests have been implemented and executed to validate app functionality, user flows, and reliability across core features.

---

## 🏗 Project Architecture & File Structure

```text
4499GRILL
├── app
│   ├── src/main/java/com/example/a4499grill
│   │   ├── SplashActivity.kt        (App Entry & Theme Loading)
│   │   ├── MainActivity.kt          (Sign-In, including SSO)
│   │   ├── RegisterActivity.kt      (Account Creation)
│   │   ├── HomeActivity.kt          (Dashboard & Favorites)
│   │   ├── MenuActivity.kt          (Full Menu Discovery)
│   │   ├── ItemDetailActivity.kt    (Customization & Basket Add)
│   │   ├── CartActivity.kt          (Basket Management)
│   │   ├── OrdersActivity.kt        (History & Multi-Payment)
│   │   ├── CommunityActivity.kt     (Social Feed & Interaction)
│   │   ├── AIChatActivity.kt        (Multilingual AI Recommendations)
│   │   ├── ProfileActivity.kt       (Settings, Language & Theme Control)
│   │   ├── Models.kt                (Data Structures: Order, Post, User)
│   │   └── CartManager.kt           (Singleton Basket Logic)
│   └── src/main/res
│       ├── layout/                      (UI XML Definitions)
│       ├── drawable/                    (Vector Icons & PNG Assets)
│       ├── values/                      (Default Strings, Colors & Light Theme)
│       ├── values-af/                   (Afrikaans Resources)
│       ├── values-zu/                   (isiZulu Resources)
│       └── values-night/                (Premium Dark Theme)
└── build.gradle                         (Project Dependencies)
```

---

## 💎 What Makes This App Unique?

1.  **The "Social Grill":** 4499GRILL combines food ordering with a community where users can rate and comment on their dining experiences.
2.  **Serverless Real-Time Sync:** Firestore snapshot listeners keep relevant data, including order status, updated in real time.
3.  **Inclusive, Multilingual Experience:** English, Afrikaans, and isiZulu support extends to the AI chatbot, helping users engage with the app in their preferred language.
4.  **Flexible Authentication and Media:** Single Sign-On simplifies access, while Firebase Storage provides blob/object storage for app and community media.
5.  **Quality Assurance:** Automated testing has been completed to support reliability and confirm core app functions work as expected.
6.  **Hybrid Logic:** The app uses a local-first fallback strategy so the interface can remain useful when cloud services are unavailable.

---

## 🛠 Tech Stack: SDKs & APIs

*   **Android SDK (Kotlin):** The foundation for modern Android development.
*   **Firebase Authentication:** Supports secure sign-in, including Single Sign-On.
*   **Cloud Firestore (NoSQL):** Stores app data and supports real-time synchronization.
*   **Firebase Storage:** Blob/object storage for food imagery and user-uploaded community media.
*   **Glide:** Image loading, cropping, and memory-efficient caching.
*   **Material Design 3:** UI components and patterns designed for accessibility and usability.
*   **Android localization resources:** Supports English, Afrikaans, and isiZulu across the app, including the chatbot experience.
*   **Automated Testing:** Included as part of the verification and quality assurance process.

---
*Developed for 4499GRILL - Premium Taste, Digital Precision.*
