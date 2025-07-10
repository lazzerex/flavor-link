# FlavorLink

A modern, feature-rich recipe discovery and cooking companion app built with Flutter. This application provides an intuitive interface for browsing, searching, and cooking with a curated collection of recipes from professional chefs.

![image](https://github.com/user-attachments/assets/10bb02dc-ee5d-4a63-8c66-770f63c5abb6)


## Table of Contents

- [Features](#features)
- [Screenshots](#screenshots)
- [Getting Started](#getting-started)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [Dependencies](#dependencies)
- [Architecture](#architecture)
- [Contributing](#contributing)
- [License](#license)

## Features

### Core Functionality
- **Recipe Discovery**: Browse curated recipes with high-quality images and detailed information
- **Advanced Search**: Real-time search with filtering by ingredients, categories, and dietary preferences
- **Favorites Management**: Save and organize favorite recipes with swipe gestures
- **Step-by-Step Cooking**: Interactive cooking mode with progress tracking
- **Timer Integration**: Built-in cooking timers for precise meal preparation
- **Chef Profiles**: Follow professional chefs and discover their signature recipes

### User Experience
- **Animated Interface**: Smooth transitions and micro-interactions throughout the app
- **Responsive Design**: Optimized for various screen sizes and orientations
- **Haptic Feedback**: Enhanced tactile experience with device vibrations
- **Dark/Light Themes**: Automatic theme switching based on system preferences
- **Offline Support**: Access saved recipes without internet connection

### Recipe Management
- **Detailed Recipe Cards**: Comprehensive information including cook time, difficulty, and nutritional data
- **Ingredient Lists**: Interactive checklists with shopping cart integration
- **Cooking Instructions**: Clear, numbered steps with completion tracking
- **Rating System**: User reviews and ratings for recipe quality
- **Social Sharing**: Share favorite recipes across social platforms

### User Profile
- **Personal Dashboard**: Track cooking achievements and favorite recipes
- **Achievement System**: Unlock badges for cooking milestones
- **Recipe History**: View previously cooked meals
- **Preference Settings**: Customize dietary restrictions and preferences

## Screenshots

![image](https://github.com/user-attachments/assets/73dd49f7-5a97-4afb-baf0-0604edf972f3)

![image](https://github.com/user-attachments/assets/c029c6e0-8d7e-466d-bb28-24acd3a66533)

![image](https://github.com/user-attachments/assets/3b7a8ed0-458a-4527-a715-d59ec1d99070)

![image](https://github.com/user-attachments/assets/a403a09e-c095-43b4-a7c9-ba22196f52c1)

![image](https://github.com/user-attachments/assets/573f1897-86bd-43b6-bf97-d71a6447575b)


## Getting Started

These instructions will help you set up the project on your local machine for development and testing purposes.

### Prerequisites

Before running this application, ensure you have the following installed:

- **Flutter SDK** (3.0.0 or higher)
- **Dart SDK** (2.17.0 or higher)
- **Android Studio** or **Visual Studio Code** with Flutter extensions
- **iOS Simulator** (for macOS users) or **Android Emulator**

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/lazzerex/flavor-link.git
   cd flavor-link
   ```

2. **Install dependencies**
   ```bash
   flutter pub get
   ```

3. **Run the app**
   ```bash
   flutter run
   ```

4. **Build for production**
   ```bash
   # Android
   flutter build apk --release
   
   # iOS
   flutter build ios --release
   ```


## Dependencies

### Core Dependencies
```yaml
flutter:
  sdk: flutter

cupertino_icons: ^1.0.2
```

### Development Dependencies
```yaml
flutter_test:
  sdk: flutter

flutter_lints: ^2.0.0
```

### Additional Packages (if using external packages)
```yaml
# State Management
provider: ^6.0.3
bloc: ^8.1.0

# Networking
http: ^0.13.5
dio: ^4.0.6

# Local Storage
shared_preferences: ^2.0.15
sqflite: ^2.2.8

# UI Enhancement
cached_network_image: ^3.2.1
shimmer: ^2.0.0
lottie: ^1.4.1

# Utilities
intl: ^0.17.0
```

## Architecture

This application follows the **Model-View-Controller (MVC)** pattern with separation of concerns:

### Data Layer
- **Models**: Define data structures for recipes, users, and application state
- **Services**: Handle API communication, local storage, and business logic
- **Repositories**: Abstract data sources and provide clean interfaces

### Presentation Layer
- **Screens**: Full-page UI components representing app sections
- **Widgets**: Reusable UI components with specific functionality
- **Controllers**: Manage state and coordinate between UI and data layers

### Key Design Patterns
- **Singleton Pattern**: For service classes and app-wide state
- **Observer Pattern**: For reactive UI updates
- **Factory Pattern**: For creating different types of recipe cards
- **Strategy Pattern**: For different search and filtering algorithms

## API Integration

The app is designed to work with a REST API for recipe data. Key endpoints include:

```
GET /api/recipes              # Fetch all recipes
GET /api/recipes/{id}         # Get specific recipe
GET /api/recipes/search       # Search recipes
GET /api/chefs                # Get chef profiles
POST /api/favorites           # Add to favorites
DELETE /api/favorites/{id}    # Remove from favorites
```

## Testing

Run the test suite with:

```bash
# Unit tests
flutter test

# Integration tests
flutter test integration_test/

# Widget tests
flutter test test/widget_test.dart
```

## Performance Considerations

- **Image Optimization**: Cached network images with progressive loading
- **Lazy Loading**: Recipes loaded on-demand as user scrolls
- **Memory Management**: Proper disposal of controllers and animations
- **State Management**: Efficient state updates to minimize rebuilds

## Accessibility

The app includes comprehensive accessibility features:

- **Screen Reader Support**: Semantic labels for all interactive elements
- **High Contrast**: Support for system accessibility settings
- **Font Scaling**: Responsive text sizing based on user preferences
- **Keyboard Navigation**: Full app navigation without touch input

## Contributing

We welcome contributions to improve the Recipe App. Please follow these steps:

1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/amazing-feature
   ```
3. **Make your changes**
4. **Add tests** for new functionality
5. **Commit your changes**
   ```bash
   git commit -m 'Add some amazing feature'
   ```
6. **Push to the branch**
   ```bash
   git push origin feature/amazing-feature
   ```
7. **Open a Pull Request**

### Code Style Guidelines

- Follow the [Dart Style Guide](https://dart.dev/guides/language/effective-dart/style)
- Use meaningful variable and function names
- Add documentation comments for public APIs
- Ensure code passes all linting rules
- Write unit tests for new features

### Commit Message Convention

Use conventional commits for clear project history:

```
feat: add recipe sharing functionality
fix: resolve animation performance issue
docs: update installation instructions
style: format code according to style guide
refactor: simplify recipe card component
test: add unit tests for search functionality
```

## Roadmap

### Upcoming Features
- **Recipe Video Tutorials**: Integrated cooking videos
- **Meal Planning**: Weekly meal planning and grocery lists
- **Social Features**: User-generated content and recipe sharing
- **AI Recommendations**: Personalized recipe suggestions
- **Voice Commands**: Hands-free cooking assistance
- **Nutritional Analysis**: Detailed macro and micronutrient tracking

### Technical Improvements
- **Backend Integration**: Connect to production API
- **Push Notifications**: Recipe reminders and updates
- **Offline Sync**: Bi-directional data synchronization
- **Performance Optimization**: Advanced caching strategies
- **Analytics Integration**: User behavior tracking

## Troubleshooting

### Common Issues

**Flutter version conflicts**
```bash
flutter clean
flutter pub get
```

**Build failures on iOS**
```bash
cd ios
pod install
cd ..
flutter build ios
```

**Android build issues**
```bash
flutter clean
cd android
./gradlew clean
cd ..
flutter build apk
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- **Flutter Team** for the excellent framework
- **Unsplash** for high-quality recipe images
- **Material Design** for design inspiration
- **Open Source Community** for various packages and tools

## Contact

**Project Maintainer**: Lazzerex

**Email**: nambinh236@gmail.com

**GitHub**: [@lazzerex](https://github.com/lazzerex)  

---

**Built with Flutter** | **Made with passion for cooking and technology**
