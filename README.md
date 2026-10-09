# Roman Yatsenko

**Senior Flutter & Mobile Engineer**

Mobile development since 2013 · Flutter since 2019

I specialize in Flutter and native mobile development, with a focus on
application architecture, maintainability, and automated testing.

Most of my recent professional work has been in private commercial
codebases, including large multi-application Flutter monorepos,
shared application architecture, and offline-first systems.

My earlier public projects are preserved with their original code
and commit histories. They show the engineering practices I was
already using years ago, from Android architecture, dependency
injection, and automated testing in 2018 to Flutter state management
and unit, widget, and integration testing in 2019.

I also started contributing to open-source Flutter packages in 2019,
with changes reviewed and merged by their maintainers.

## Open-Source Contributions

### FlutterYoutube (2019)

**[Merged PR #53: Android Action Bar Visibility](https://github.com/ponnamkarthik/FlutterYoutube/pull/53)**

Added configurable Android Action Bar visibility to a Flutter
YouTube player plugin.

The changes covered the public Dart API, Flutter platform channel
communication, and native Android Java implementation.

An upstream reviewer commented "Perfect." on the Android changes,
and the maintainer merged the PR in December 2019.

[View the original review and merged code](https://github.com/ponnamkarthik/FlutterYoutube/pull/53)

### Flutter Fortune Wheel (2023)

**[Merged PR #107: Haptic Feedback & Gesture Physics](https://github.com/kevlatus/flutter_fortune_wheel/pull/107)**

Extended the Flutter package with:

- Configurable haptic feedback when crossing wheel sections.
- Gesture behavior controlling the direction of user-initiated rotation.

The maintainer approved the PR, describing the haptic feedback
implementation as "simple, yet effective".

The functionality was released in `flutter_fortune_wheel` 1.3.0,
with an explicit acknowledgment of @YatsenkoDev in the
official package changelog.

**[View the release notes on pub.dev](https://pub.dev/packages/flutter_fortune_wheel/changelog#130---2023-07-04)**

### Flutter Health Plugin (2024)

**[View implementation](https://github.com/YatsenkoDev/flutter-plugins)**

Implemented cross-platform health data aggregation methods
in a public fork of a Flutter plugin:

- `getTotalCaloriesInInterval`
- `getTotalDistanceInInterval`

The implementation uses native Android and iOS health APIs
to calculate aggregated values over a specified time interval.

**Original implementations:**

[Android](https://github.com/YatsenkoDev/flutter-plugins/commit/2109de07dab4a1fb4516dee1b18becceeba1e3eb) ·
[iOS](https://github.com/YatsenkoDev/flutter-plugins/commit/dd79d909fd969db7b40b548a6e0836b6a13558e3) ·
[Upstream discussion](https://github.com/carp-dk/carp-health-flutter/issues/177)

## Earlier Engineering Work

### Transformer Arena (Android, 2018)

**[Source Code](https://github.com/YatsenkoDev/Transformer-Arena)**

Java · MVP · Dagger · RxJava · JUnit · Mockito · Espresso

A native Android application featuring:

- MVP-style separation of presentation and service responsibilities.
- Dependency injection and reactive programming.
- Unit testing of presenters and application services.
- UI testing with Espresso.

**[Original unit-test implementation, October 2018](https://github.com/YatsenkoDev/Transformer-Arena/commit/b1de7133b29cdf1a09595f728fd227fd7256c4ef)**

### Chorus (Flutter, 2019)

**[Source Code](https://github.com/YatsenkoDev/chorus)**

Flutter · Dart · BLoC · RxDart · Provider

An early Flutter video player application featuring:

- BLoC-based state management and reactive streams.
- API integration and asynchronous data processing.
- Resource lifecycle management.
- Unit, widget, and integration testing.

**Original tests:**

[Unit & widget tests](https://github.com/YatsenkoDev/chorus/commit/1172667) ·
[Integration test](https://github.com/YatsenkoDev/chorus/commit/4046baa)

### Instagram Preview (Flutter, 2019-2020)

**[Source Code](https://github.com/YatsenkoDev/Instagram-preview)**

Flutter · Dart · Provider · RxDart · Hive

An early Flutter application featuring:

- Instagram API integration.
- Reactive state management.
- Local persistence with Hive.
- Interactive photo reordering using drag-and-drop.

**[Original drag-and-drop implementation, January 2020](https://github.com/YatsenkoDev/Instagram-preview/commit/af7f245810dd85124a9b27ddc35be7e94a4ed500)**

## Technical Walkthroughs

More detailed notes on the projects and contributions above,
with links to original source code, tests, commits, and code reviews.

- **[Transformer Arena: Android Engineering (2018)](portfolio/transformer-arena.md)**  
  MVP architecture, Dagger dependency injection, RxJava, lifecycle
  management, and JUnit/Mockito/Espresso tests from 2018.

- **[Chorus: Flutter Engineering (2019)](portfolio/chorus.md)**  
  Early Flutter development with BLoC, RxDart, Provider,
  asynchronous APIs, and unit, widget, and integration tests.

- **[Instagram Preview: Flutter Engineering (2019-2020)](portfolio/instagram-preview.md)**  
  Reactive state management, REST API integration, Hive persistence,
  and drag-and-drop photo reordering.

- **[Flutter Open-Source Contributions (2019-2024)](portfolio/open-source-contributions.md)**  
  Two merged Flutter package PRs, external code reviews,
  a published acknowledgment on pub.dev, and native Android/iOS
  health plugin development.
