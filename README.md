# DigiLife Hub 🏠

> A comprehensive digital life management application built with Flutter

DigiLife Hub is a modern mobile application designed to help users manage their digital subscriptions, track expenses, and optimize their digital spending. Built with Flutter and Firebase, it offers a seamless experience across iOS and Android platforms.

## ✨ Features

### 📊 Subscription Management
- **Complete CRUD Operations**: Add, edit, delete, and view all your subscriptions
- **Smart Categorization**: Organize subscriptions by type (Streaming, Software, Gaming, etc.)
- **Cost Tracking**: Monitor monthly and annual expenses
- **Payment Calendar**: Never miss a payment with integrated calendar view
- **Status Management**: Track active, inactive, trial, and expiring subscriptions

### 🤖 Automatic Detection
- **Email Analysis**: Automatically detect subscriptions from Gmail
- **Bank Statement Import**: Upload CSV files to discover recurring payments
- **Template Catalog**: Choose from popular subscription services
- **Smart Recognition**: AI-powered detection with confidence scoring

### 🔥 One-Click Cancellation
- **Automated Cancellation**: Cancel supported subscriptions directly from the app
- **Service Integration**: Direct API integration with major providers
- **Cancellation History**: Track all cancellation requests and their status
- **Support Check**: Verify which services support automatic cancellation

### 🔐 Advanced Authentication
- **Multiple Login Methods**: Email/password, Google, Apple Sign-In
- **Biometric Authentication**: Fingerprint and Face ID support
- **Secure Storage**: Encrypted credential storage
- **Password Reset**: Easy password recovery flow

### 📱 Modern UI/UX
- **Material Design 3**: Latest Google design principles
- **Dark/Light Theme**: Automatic theme switching
- **Responsive Design**: Optimized for all screen sizes
- **Smooth Animations**: Fluid transitions and micro-interactions
- **Accessibility**: Full accessibility support

## 🏗️ Architecture

DigiLife Hub follows **Clean Architecture** principles with clear separation of concerns:

```
lib/
├── core/                   # Core utilities and shared code
│   ├── constants/         # App constants and themes
│   ├── errors/           # Error handling and failures
│   └── usecases/         # Base usecase classes
├── data/                  # Data layer
│   ├── models/           # Data models
│   └── repositories/     # Repository implementations
├── domain/               # Domain layer (business logic)
│   ├── entities/         # Business entities
│   ├── repositories/     # Repository interfaces
│   └── usecases/         # Business use cases
├── features/             # Feature-specific modules
│   ├── subscription_detection/  # Auto-detection feature
│   └── subscription_cancellation/  # Cancellation feature
└── presentation/         # Presentation layer
    ├── blocs/           # BLoC state management
    ├── pages/           # UI screens
    └── widgets/         # Reusable UI components
```

## 🛠️ Tech Stack

- **Framework**: Flutter 3.0+
- **Language**: Dart
- **State Management**: Flutter BLoC
- **Backend**: Firebase (Auth, Firestore)
- **Local Storage**: Hive, Secure Storage, SharedPreferences
- **Authentication**: Firebase Auth, Google Sign-In, Local Auth
- **UI**: Material Design 3, Google Fonts
- **Data Visualization**: FL Chart
- **Architecture**: Clean Architecture with Dependency Injection

## 🚀 Getting Started

### Prerequisites

- Flutter SDK (3.0 or higher)
- Dart SDK (3.0 or higher)
- Firebase project setup
- Android Studio / VS Code
- iOS development: Xcode (for iOS builds)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/digilife-hub.git
   cd digilife-hub
   ```

2. **Install dependencies**
   ```bash
   flutter pub get
   ```

3. **Firebase Setup**
   ```bash
   # Install Firebase CLI
   npm install -g firebase-tools
   
   # Login to Firebase
   firebase login
   
   # Configure Firebase for Flutter
   flutterfire configure
   ```

4. **Generate required files**
   ```bash
   flutter packages pub run build_runner build
   ```

5. **Run the application**
   ```bash
   flutter run
   ```

## 🔧 Configuration

### Firebase Configuration

1. Create a new Firebase project
2. Enable Authentication (Email/Password, Google, Apple)
3. Set up Firestore database
4. Add your app to Firebase project
5. Download and place configuration files:
   - `android/app/google-services.json`
   - `ios/Runner/GoogleService-Info.plist`

### Environment Variables

Create a `.env` file in the root directory:

```env
# API Keys (if needed)
API_KEY=your_api_key_here

# Feature Flags
ENABLE_ANALYTICS=true
ENABLE_CRASH_REPORTING=true
```

## 📱 Features Walkthrough

### Subscription Management
- Add subscriptions manually or through detection
- Set reminders for upcoming payments
- Track spending with visual charts
- Export data for analysis

### Automatic Detection
1. **Email Detection**: Connect Gmail account to scan for subscription emails
2. **CSV Import**: Upload bank statements to find recurring payments
3. **Template Selection**: Browse catalog of popular services

### Cancellation Flow
1. Select subscription to cancel
2. App checks if automatic cancellation is supported
3. Enter service credentials securely
4. Automatic cancellation request submitted
5. Track cancellation status in history

## 🧪 Testing

Run the test suite:

```bash
# Unit tests
flutter test

# Integration tests
flutter test integration_test/

# Generate coverage report
flutter test --coverage
genhtml coverage/lcov.info -o coverage/html
```

## 🚀 Deployment

### Android
```bash
flutter build apk --release
# or
flutter build appbundle --release
```

### iOS
```bash
flutter build ios --release
```

### Web
```bash
flutter build web --release
```

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for details.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Authors

- **Your Name** - *Initial work* - [YourGitHub](https://github.com/yourusername)

## 🙏 Acknowledgments

- Flutter team for the amazing framework
- Firebase for backend services
- Material Design team for design guidelines
- All contributors who helped improve this project

## 📞 Support

If you encounter any issues or have questions:

1. Check the [Issues](https://github.com/yourusername/digilife-hub/issues) page
2. Create a new issue if your problem isn't already reported
3. Join our [Discord community](https://discord.gg/yourinvite) for real-time help

## 🗺️ Roadmap

- [ ] **v1.1**: Advanced analytics and insights
- [ ] **v1.2**: Multi-language support
- [ ] **v1.3**: Family sharing features
- [ ] **v1.4**: AI-powered spending recommendations
- [ ] **v1.5**: Third-party integrations (Mint, YNAB)

## 📊 Screenshots

<details>
<summary>Click to view screenshots</summary>

| Home Screen | Subscription List | Detection Flow |
|-------------|-------------------|----------------|
| ![Home](screenshots/home.png) | ![List](screenshots/list.png) | ![Detection](screenshots/detection.png) |

| Cancellation | Calendar | Profile |
|--------------|----------|---------|
| ![Cancel](screenshots/cancel.png) | ![Calendar](screenshots/calendar.png) | ![Profile](screenshots/profile.png) |

</details>

---

<p align="center">
  Made with ❤️ using Flutter
</p>
