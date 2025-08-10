# Week 4: API Integration and Networking

A comprehensive Flutter application demonstrating HTTP requests, JSON parsing, and data display with proper error handling and loading states.

## 🎯 Learning Objectives

This project covers the following key concepts:

- **HTTP Requests and JSON Parsing**: Using the `http` package to fetch data from RESTful APIs
- **Data Models**: Creating structured models for API responses with proper JSON serialization
- **Error Handling**: Implementing robust error handling for failed API requests
- **Loading States**: Displaying appropriate loading indicators during data fetching
- **Professional UI/UX**: Building a modern, responsive interface with Material Design 3

## 🚀 Features

### 1. Home Screen
- **Modern Dashboard**: Beautiful gradient header with app overview
- **Navigation Cards**: Easy access to different app features
- **Feature Overview**: Clear explanation of what the app demonstrates

### 2. Users List Screen
- **API Integration**: Fetches all users from JSONPlaceholder API
- **ListView Display**: Shows users in beautiful, interactive cards
- **Pull-to-Refresh**: Swipe down to refresh the user list
- **Error Handling**: Displays user-friendly error messages with retry options
- **Loading States**: Shows loading spinners during data fetching

### 3. User Profile Search Screen
- **Search Functionality**: Search for specific users by ID (1-10)
- **Form Validation**: Input validation with helpful error messages
- **Real-time Results**: Immediate display of search results
- **Quick Profile View**: Compact user information display
- **Navigation**: Easy access to full user profiles

### 4. User Detail Screen
- **Tabbed Interface**: Three organized tabs for different information types
- **Profile Tab**: Complete user information including contact and company details
- **Address Tab**: Detailed address information with geographic coordinates
- **Posts Tab**: User's posts fetched from the API
- **Responsive Design**: Adapts to different screen sizes

## 🏗️ Architecture

### Project Structure
```
lib/
├── main.dart                 # App entry point
├── models/
│   └── user.dart            # User data models
├── services/
│   └── api_service.dart     # API communication layer
└── screens/
    ├── home_screen.dart      # Main navigation hub
    ├── users_list_screen.dart # Users list with API integration
    ├── user_profile_screen.dart # User search functionality
    └── user_detail_screen.dart  # Detailed user information
```

### Key Components

#### Models (`lib/models/user.dart`)
- **User**: Main user model with all profile information
- **Address**: Nested address model with geographic coordinates
- **Company**: Company information model
- **Geo**: Geographic coordinates model
- **JSON Serialization**: Proper `fromJson` and `toJson` methods

#### API Service (`lib/services/api_service.dart`)
- **HTTP Client**: Uses the `http` package for API requests
- **Error Handling**: Comprehensive error handling with timeout support
- **Multiple Endpoints**: Fetches users, individual users, and posts
- **Type Safety**: Proper typing for all API responses

#### UI Components
- **Material Design 3**: Modern, adaptive design system
- **Responsive Layouts**: Works on various screen sizes
- **Loading States**: Professional loading indicators
- **Error States**: User-friendly error messages with recovery options

## 🛠️ Technical Implementation

### Dependencies
```yaml
dependencies:
  flutter:
    sdk: flutter
  cupertino_icons: ^1.0.8
  http: ^1.1.0  # For API requests
```

### API Integration
- **Base URL**: `https://jsonplaceholder.typicode.com`
- **Endpoints**:
  - `GET /users` - Fetch all users
  - `GET /users/{id}` - Fetch specific user
  - `GET /posts?userId={id}` - Fetch user posts
- **Timeout**: 10 seconds for all requests
- **Error Handling**: Network errors, HTTP status codes, and parsing errors

### State Management
- **StatefulWidget**: Local state management for each screen
- **setState**: Efficient UI updates during data loading
- **Async Operations**: Proper handling of asynchronous API calls

### Error Handling Strategy
1. **Network Errors**: Connection issues and timeouts
2. **HTTP Errors**: Non-200 status codes
3. **Parsing Errors**: Invalid JSON responses
4. **User Feedback**: Clear error messages with recovery options

## 📱 User Experience Features

### Loading States
- **Circular Progress Indicators**: During initial data loading
- **Skeleton Loading**: Placeholder content while fetching
- **Refresh Indicators**: Visual feedback during pull-to-refresh

### Error Recovery
- **Retry Buttons**: Easy retry for failed requests
- **Clear Error States**: Automatic error clearing on successful operations
- **User Guidance**: Helpful messages explaining what went wrong

### Navigation
- **Intuitive Flow**: Logical screen progression
- **Back Navigation**: Standard Android/iOS navigation patterns
- **Deep Linking**: Direct access to user profiles

## 🎨 Design Principles

### Material Design 3
- **Color Scheme**: Adaptive color system with light/dark themes
- **Typography**: Consistent text hierarchy and readability
- **Spacing**: Proper margins and padding for visual breathing room
- **Elevation**: Subtle shadows and depth for interactive elements

### Responsive Design
- **Flexible Layouts**: Adapts to different screen sizes
- **Grid Systems**: Responsive grid for feature cards
- **Touch Targets**: Proper sizing for mobile interaction

### Accessibility
- **Semantic Labels**: Proper labeling for screen readers
- **Color Contrast**: Sufficient contrast ratios
- **Touch Feedback**: Visual feedback for all interactive elements

## 🚀 Getting Started

### Prerequisites
- Flutter SDK (3.7.0 or higher)
- Dart SDK
- Android Studio / VS Code with Flutter extensions

### Installation
1. Clone the repository
2. Navigate to the project directory
3. Install dependencies:
   ```bash
   flutter pub get
   ```
4. Run the application:
   ```bash
   flutter run
   ```

### Testing
- **Unit Tests**: Test models and API service
- **Widget Tests**: Test UI components
- **Integration Tests**: Test complete user flows

## 📚 Learning Outcomes

After completing this project, you will understand:

1. **HTTP Package Usage**: How to make API requests in Flutter
2. **JSON Parsing**: Converting API responses to Dart objects
3. **Error Handling**: Managing network failures and API errors
4. **Loading States**: Providing user feedback during operations
5. **State Management**: Managing application state effectively
6. **UI/UX Design**: Creating professional, user-friendly interfaces

## 🔧 Customization

### Adding New APIs
1. Create new models in the `models/` directory
2. Add API methods in `api_service.dart`
3. Create corresponding UI screens
4. Update navigation in `home_screen.dart`

### Styling Changes
- Modify theme colors in `main.dart`
- Update component styles in individual screen files
- Customize Material Design 3 components

### Additional Features
- **Caching**: Implement local storage for offline access
- **Pagination**: Add pagination for large data sets
- **Search**: Implement global search functionality
- **Favorites**: Add user bookmarking feature

## 🤝 Contributing

This project serves as a learning resource for Flutter developers. Feel free to:

- Fork the repository
- Add new features
- Improve error handling
- Enhance the UI/UX
- Add tests
- Update documentation

## 📄 License

This project is created for educational purposes as part of a Flutter learning curriculum.

## 🙏 Acknowledgments

- **JSONPlaceholder**: Free fake API for testing and prototyping
- **Flutter Team**: Amazing framework and documentation
- **Material Design**: Design system and guidelines

---

**Happy Coding! 🎉**

This application demonstrates professional Flutter development practices and serves as a solid foundation for building production-ready apps with API integration.
