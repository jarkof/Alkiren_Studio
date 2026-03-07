# Alkiren Studio: Standard Technical Stack

## Core Environment
- **Language**: Java 11+ (Strictly no Kotlin).
- **Minimum SDK**: API 26 (Android 8.0).
- **Target/Compile SDK**: API 36 (Android 16).
- **Build System**: Gradle (Kotlin DSL preferred for build scripts).

## Mandatory Libraries
- **UI Framework**: AndroidX AppCompat, Material Components, ConstraintLayout.
- **Splash Screen**: `androidx.core:core-splashscreen` (Migrating away from legacy SplashActivity).
- **Ads**: AppLovin MAX SDK (Alternative to AdMob).
- **Images/Media**: Glide (for loading) and Exifinterface.

## Testing Framework
- **Unit Testing**: JUnit 4/5.
- **Mocking**: Mockito for dependency isolation.
- **Instrumentation**: Espresso for critical UI flow verification.

## Architectural Patterns
- **Pattern**: Clean Architecture / MVVM.
- **Dependency Management**: Manual Constructor Injection to maintain 100% testability.
