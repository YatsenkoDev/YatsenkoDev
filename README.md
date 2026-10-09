# Roman Yatsenko

**Senior Flutter & Mobile Engineer**

Mobile development since 2013 · Flutter since 2019

I specialize in Flutter and native mobile development, with a focus on
application architecture, maintainability, and automated testing.

Most of my recent professional work has been in private commercial
codebases, including large multi-application Flutter monorepos,
shared application architecture, and offline-first systems.

My earlier public projects are intentionally preserved in their
original state. Their commit histories show the engineering practices
I was already applying years ago — from Android architecture,
dependency injection, and automated testing in 2018 to Flutter
state management and unit, widget, and integration testing in 2019.

Alongside these historical projects, this profile documents my
later contributions to the Flutter open-source ecosystem.

## Open-Source Contributions

### Flutter Fortune Wheel — Merged Contribution (2023)

**[Merged PR #107 — Haptic Feedback & Gesture Physics](https://github.com/kevlatus/flutter_fortune_wheel/pull/107)**

Extended a community Flutter package with:

- Configurable haptic feedback when crossing wheel sections.
- Gesture behavior controlling the direction of user-initiated rotation.

The contribution was reviewed, approved, and merged by the
project maintainer.

**Maintainer feedback:**
> "simple, yet effective implementation of haptic feedback"

The haptic feedback functionality was included in version 1.3.0,
with an explicit acknowledgment of @YatsenkoDev in the official
package changelog.

**[View the official release notes on pub.dev](https://pub.dev/packages/flutter_fortune_wheel/changelog#130---2023-07-04)**

### Flutter Health Plugin — Native Platform Integration (2024)

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

These projects provide verifiable examples of the technologies,
architectural patterns, and testing practices I was using
during my earlier years of mobile development.

The original source code and commit histories remain unchanged.

### Transformer Arena — Native Android (2018)

**[Source Code](https://github.com/YatsenkoDev/Transformer-Arena)**

Java · MVP · Dagger · RxJava · JUnit · Mockito · Espresso

A native Android application featuring:

- MVP-style separation of presentation and service responsibilities.
- Dependency injection and reactive programming.
- Unit testing of presenters and application services.
- UI testing with Espresso.

**Historical evidence:**
[Original October 2018 unit-test implementation](https://github.com/YatsenkoDev/Transformer-Arena/commit/b1de7133b29cdf1a09595f728fd227fd7256c4ef)

### Chorus — Flutter (2019)

**[Source Code](https://github.com/YatsenkoDev/chorus)**

Flutter · Dart · BLoC · RxDart · Provider

An early Flutter application demonstrating:

- BLoC-based state management and reactive streams.
- API integration and asynchronous data processing.
- Resource lifecycle management.
- Unit, widget, and integration testing.

**Historical evidence:**
[Unit & widget tests](https://github.com/YatsenkoDev/chorus/commit/1172667) ·
[Integration test](https://github.com/YatsenkoDev/chorus/commit/4046baa)

### Instagram Preview — Flutter (2019–2020)

**[Source Code](https://github.com/YatsenkoDev/Instagram-preview)**

Flutter · Dart · Provider · RxDart · Hive

An early Flutter application featuring:

- Instagram API integration.
- Reactive state management.
- Local persistence with Hive.
- Interactive photo reordering using drag-and-drop.

**Historical evidence:**
[Original drag-and-drop implementation (January 2020)](https://github.com/YatsenkoDev/Instagram-preview/commit/af7f245810dd85124a9b27ddc35be7e94a4ed500)

---

## Technical Walkthroughs

Detailed examinations of selected projects and open-source contributions,
with direct links to original source code, historical commits, automated
tests, and external code reviews.

- **[Transformer Arena — Android Engineering (2018)](portfolio/transformer-arena.md)**  
  MVP architecture, Dagger dependency injection, RxJava, lifecycle management,
  and JUnit/Mockito/Espresso testing — with original 2018 code references.

- **[Chorus — Flutter Engineering (2019)](portfolio/chorus.md)**  
  Early Flutter development with BLoC, RxDart, Provider, asynchronous APIs,
  and unit, widget, and integration tests from 2019.

- **[Instagram Preview — Flutter Engineering (2019–2020)](portfolio/instagram-preview.md)**  
  Reactive state management, REST API integration, Hive persistence,
  and drag-and-drop photo reordering implemented in early 2020.

- **[Flutter Open-Source Contributions (2023–2024)](portfolio/open-source-contributions.md)**  
  Merged Flutter Fortune Wheel PR, positive maintainer review, official
  pub.dev release acknowledgment, and cross-platform Health plugin development.

---

*Historical projects are preserved as examples of my work at the
time they were developed, rather than maintained as references
for current framework best practices.*
