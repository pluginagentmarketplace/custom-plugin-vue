---
name: mobile-development
description: Master iOS, Android, and cross-platform mobile development including Swift, Kotlin, React Native, and Flutter. Use when building mobile apps, optimizing performance, or choosing mobile technologies.
---

# Mobile Development

## Quick Start

Mobile development combines platform-specific and cross-platform approaches:

```swift
// SwiftUI Example for iOS
import SwiftUI

struct ContentView: View {
    @State private var count = 0

    var body: some View {
        VStack(spacing: 20) {
            Text("Counter App")
                .font(.title)

            Text("\(count)")
                .font(.system(size: 60, weight: .bold))

            HStack(spacing: 20) {
                Button(action: { count -= 1 }) {
                    Image(systemName: "minus.circle")
                        .font(.title)
                }

                Button(action: { count += 1 }) {
                    Image(systemName: "plus.circle")
                        .font(.title)
                }
            }
        }
        .padding()
    }
}
```

## iOS Development

### Swift Fundamentals
- **Variables & Types**: let/var, optionals, error handling
- **Functions**: Parameters, return types, closures
- **Object-Oriented**: Classes, structs, inheritance, protocols
- **Generics**: Type-safe, reusable code

### SwiftUI Framework
- **View Protocol**: Building UI components
- **State Management**: @State, @ObservedObject, @EnvironmentObject
- **Layout**: VStack, HStack, ZStack, custom layouts
- **Animations**: Implicit and explicit animations
- **Navigation**: NavigationStack, NavigationLink

### iOS App Architecture
- **MVC**: Model-View-Controller pattern
- **MVVM**: Model-View-ViewModel with reactive binding
- **Clean Architecture**: Separation of concerns
- **Dependency Injection**: Loose coupling

### Core Features
- **Networking**: URLSession for API calls
- **Local Storage**: UserDefaults, Core Data, Realm
- **Background Tasks**: Background fetch, silent notifications
- **Hardware**: Camera, sensors, GPS, Bluetooth

## Android Development

### Kotlin Essentials
- **Variables**: val/var, nullable types
- **Functions**: Default parameters, extension functions
- **Classes**: Data classes, sealed classes, objects
- **Coroutines**: Async/await style concurrency

### Jetpack Components
- **Compose**: Modern declarative UI framework
- **Navigation**: Fragment transactions, nav graphs
- **Room**: SQLite abstraction
- **WorkManager**: Background task scheduling
- **ViewModel**: Lifecycle-aware state management

### Android Architecture
```kotlin
// MVVM with Kotlin Coroutines
class UserViewModel : ViewModel() {
    private val _users = MutableStateFlow<List<User>>(emptyList())
    val users: StateFlow<List<User>> = _users.asStateFlow()

    fun fetchUsers() {
        viewModelScope.launch {
            try {
                val userList = repository.getUsers()
                _users.value = userList
            } catch (e: Exception) {
                // Handle error
            }
        }
    }
}
```

### Key Concepts
- **Activities & Fragments**: UI components with lifecycle
- **Intents**: Communication between components
- **Services**: Background execution
- **Content Providers**: Data sharing between apps

## Cross-Platform Development

### React Native
- **Native Modules**: Bridging to platform-specific code
- **Navigation**: React Navigation library
- **State Management**: Redux, Context API, Zustand
- **Performance**: Native views for optimal performance
- **Deployment**: App Store and Google Play

### Flutter Framework
- **Dart Language**: Type-safe, JIT and AOT compilation
- **Widgets**: Everything is a widget in Flutter
- **Hot Reload**: Fast development cycle
- **Native Performance**: Compiled to native code
- **Rich Ecosystem**: 100K+ packages available

```dart
// Flutter Example
class CounterApp extends StatefulWidget {
  @override
  _CounterAppState createState() => _CounterAppState();
}

class _CounterAppState extends State<CounterApp> {
  int counter = 0;

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(title: Text('Counter')),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: [
            Text('Count: $counter', style: TextStyle(fontSize: 48)),
            SizedBox(height: 20),
            FloatingActionButton(
              onPressed: () => setState(() => counter++),
              child: Icon(Icons.add),
            ),
          ],
        ),
      ),
    );
  }
}
```

## Mobile App Architecture

### Design Patterns
- **MVC/MVVM**: Separating concerns
- **Repository Pattern**: Abstract data access
- **Dependency Injection**: Managing dependencies
- **Observer Pattern**: Reactive updates

### State Management
- **Local State**: Widget/ViewModel state
- **Global State**: App-wide state (Redux, Provider, GetX)
- **Async State**: API responses, loading states
- **Persistence**: Local database, SharedPreferences

## Performance Optimization

### Battery & Memory
- **Reduce CPU Usage**: Efficient algorithms, background task management
- **Memory Leaks**: Proper resource cleanup
- **Image Optimization**: Compression, lazy loading
- **Background Tasks**: Intelligent scheduling

### Startup Performance
- **Lazy Loading**: Deferring initialization
- **Code Splitting**: On-demand module loading
- **Profiling**: Identifying bottlenecks

## Testing Mobile Apps

### Testing Strategies
- **Unit Tests**: Logic testing, mocking
- **Widget Tests**: UI component testing
- **Integration Tests**: End-to-end testing
- **UI Automation**: Espresso (Android), XCTest (iOS)

### Continuous Integration
- **Test Automation**: Running tests on every commit
- **Build Automation**: Automated build and signing
- **Deployment**: Beta testing, staged rollouts

## App Store & Distribution

### iOS App Store
- **App Review**: Apple's review guidelines
- **Code Signing**: Certificates and provisioning profiles
- **TestFlight**: Beta testing platform
- **Versioning**: Semantic versioning strategy

### Google Play Store
- **Review Process**: Google's policies
- **Play Console**: Distribution management
- **Beta Testing**: Android beta testing
- **Release Management**: Gradual rollouts

## Best Practices

1. **Performance**: Optimize startup, memory, battery
2. **Testing**: Comprehensive test coverage
3. **UI/UX**: Responsive, accessible, platform conventions
4. **Security**: Data encryption, secure storage
5. **Documentation**: Clear code, API documentation
6. **Analytics**: Track user behavior and crashes
7. **Updates**: Regular updates, backward compatibility

## Learning Resources

- Android Roadmap: https://roadmap.sh/android
- iOS Roadmap: https://roadmap.sh/ios
- Flutter: https://flutter.dev
- React Native: https://reactnative.dev
- Swift: https://developer.apple.com/swift
- Kotlin: https://kotlinlang.org
