# 🌿 EcoTrack: Your Personal Sustainability Companion 🌍

EcoTrack is a React-based application designed to help users track and improve their environmental footprint. It provides tools to monitor travel habits, record visits to sustainable restaurants, and visualize your overall sustainability score. EcoTrack aims to empower individuals to make more informed and eco-conscious decisions in their daily lives.

## 🚀 Key Features

- **Sustainability Score Tracking:**  Visualize your environmental impact with a dynamic sustainability score gauge.
- **Travel Habit Monitoring:**  Record your travel methods (car, bus, bike, etc.) and calculate the environmental impact of each trip.  Leverages the Gemini API to provide accurate sustainability scores.
- **Sustainable Restaurant Logging:**  Discover and log visits to sustainable restaurants, earning points based on their sustainability rating.
- **Authentication & User Profiles:** Secure user authentication to personalize the experience and track individual progress.
- **Route Protection:** Ensures that sensitive routes like dashboard and profile are only accessible to authenticated users.
- **Real-time Updates:** Utilizes Firebase's `onAuthStateChanged` to provide real-time updates on user authentication status.
- **Mobile-Friendly Navigation:** Responsive navigation component that adapts to different screen sizes.
- **Toast Notifications:** Provides user-friendly feedback through toast notifications for actions like sign-out and recording visits.
- **Dynamic Google Maps Integration:** Displays travel locations on an interactive Google Map.

## 🛠️ Tech Stack

*   **Frontend:**
    *   React
    *   React Router DOM
    *   TypeScript
    *   Vite
    *   @vitejs/plugin-react-swc
    *   lucide-react (icons)
    *   @/components/ui/\* (Custom UI components - likely Radix UI or Shadcn UI based)
    *   sonner (toast notifications)
    *   App.css, index.css
*   **Backend & Database:**
    *   Firebase
    *   Firebase Authentication
    *   Firebase Firestore
    *   Firebase Storage
*   **AI:**
    *   Google Gemini API
*   **Build Tools:**
    *   Vite
    *   TypeScript Compiler (tsc)
*   **Other:**
    *   Node.js
    *   path (Node.js module)
    *   lovable-tagger (development/debugging - conditionally included)

## 📦 Getting Started

### Prerequisites

*   Node.js (>=18)
*   npm or yarn
*   Firebase project with Authentication, Firestore, and Storage enabled
*   Google Gemini API key
*   Google Maps API key

### Installation

1.  **Clone the repository:**

    ```bash
    git clone <repository_url>
    cd <project_directory>
    ```

2.  **Install dependencies:**

    ```bash
    npm install # or yarn install
    ```

3.  **Configure Firebase:**

    *   Create a `.env` file in the root directory.
    *   Add your Firebase configuration details to the `.env` file:

    ```
    VITE_FIREBASE_API_KEY=<your_firebase_api_key>
    VITE_FIREBASE_AUTH_DOMAIN=<your_firebase_auth_domain>
    VITE_FIREBASE_PROJECT_ID=<your_firebase_project_id>
    VITE_FIREBASE_STORAGE_BUCKET=<your_firebase_storage_bucket>
    VITE_FIREBASE_MESSAGING_SENDER_ID=<your_firebase_messaging_sender_id>
    VITE_FIREBASE_APP_ID=<your_firebase_app_id>
    VITE_GOOGLE_MAPS_API_KEY=<your_google_maps_api_key>
    VITE_GEMINI_API_KEY=<your_gemini_api_key>
    ```

    *   Ensure the Firebase configuration in `src/integrations/firebase/config.ts` matches your Firebase project settings.

4.  **Configure Google Maps API Key:**

    *   Add your Google Maps API key to the `.env` file as `VITE_GOOGLE_MAPS_API_KEY`.

5.  **Configure Google Gemini API Key:**
    *   Add your Google Gemini API key to the `.env` file as `VITE_GEMINI_API_KEY`.

### Running Locally

```bash
npm run dev # or yarn dev
```

This will start the development server. Open your browser and navigate to `http://localhost:8080` (or the port specified in `vite.config.ts`).

## 📂 Project Structure

```
├── .env                    # Environment variables (API keys, Firebase config)
├── .gitignore              # Specifies intentionally untracked files that Git should ignore
├── index.html              # Main HTML file
├── package.json            # Project dependencies and scripts
├── README.md               # Project documentation
├── src                     # Source code directory
│   ├── App.css             # Styles for the App component
│   ├── App.tsx             # Main application component
│   ├── components          # Reusable React components
│   │   ├── AuthProvider.tsx    # Authentication context provider
│   │   ├── Navigation.tsx      # Navigation bar component
│   │   ├── ProtectedRoute.tsx  # Route protection component
│   │   ├── dashboard           # Dashboard related components
│   │   │   ├── RestaurantStats.tsx # Restaurant statistics component
│   │   │   ├── SustainabilityScore.tsx # Sustainability score gauge component
│   │   │   ├── TravelStats.tsx     # Travel statistics component
│   │   │   ├── TripMap.tsx         # Google Maps component for displaying travel locations
│   │   ├── ui                # UI components (likely from Radix UI or Shadcn UI)
│   │   │   ├── button.tsx        # Example: Button component
│   │   │   └── ...             # Other UI components
│   ├── context             # React context files
│   │   ├── AuthContext.tsx   # Authentication context
│   ├── integrations      # Integrations with external services
│   │   ├── firebase          # Firebase integration
│   │   │   ├── config.ts       # Firebase configuration
│   ├── main.tsx            # Entry point for the React application
│   ├── pages               # Page components for different routes
│   │   ├── About.tsx         # About page
│   │   ├── Dashboard.tsx     # Dashboard page
│   │   ├── Index.tsx         # Index page
│   │   ├── Login.tsx         # Login page
│   │   ├── NotFound.tsx      # 404 page
│   │   ├── Profile.tsx       # Profile page
│   │   ├── Register.tsx      # Register page
│   │   ├── Rewards.tsx       # Rewards page
│   ├── services            # Services for interacting with external APIs
│   │   ├── firebase.ts       # Firebase related services
│   ├── styles              # Global styles
│   ├── types               # TypeScript type definitions
│   │   ├── sustainability.ts # Type definitions for sustainability data
├── tsconfig.json         # TypeScript configuration
├── tsconfig.node.json    # TypeScript configuration for Node.js
├── tsconfig.app.json     # TypeScript configuration for the app
├── vite.config.ts        # Vite configuration file
```

## 📸 Screenshots

(Add screenshots of your application here to showcase its features and UI)

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1.  Fork the repository.
2.  Create a new branch for your feature or bug fix.
3.  Make your changes and commit them with descriptive messages.
4.  Push your changes to your fork.
5.  Submit a pull request to the main branch of the original repository.

## 📝 License

This project is licensed under the [MIT License](LICENSE).

## 📬 Contact

If you have any questions or suggestions, feel free to contact me at [your_email@example.com](mailto:your_email@example.com).

## 💖 Thanks

Thank you for checking out EcoTrack! I hope this project helps you on your journey to a more sustainable lifestyle.

This README is written by [readme.ai](https://readme-generator-phi.vercel.app/).

