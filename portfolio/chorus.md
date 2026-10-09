# Chorus — Flutter Engineering (2019)

**Flutter · Dart · BLoC · RxDart · Provider · HTTP · Automated Testing**

[Original repository](https://github.com/YatsenkoDev/chorus) |
[Original 2019 source snapshot](https://github.com/YatsenkoDev/chorus/tree/4046baa) |
[Unit & widget test commit](https://github.com/YatsenkoDev/chorus/commit/1172667) |
[Integration test commit](https://github.com/YatsenkoDev/chorus/commit/4046baa)

## Project Context

A Flutter video player application developed in 2019 as
a coding assignment.

The application retrieves video content and associated
transcripts, displaying messages alongside video playback.

This repository is preserved as a historical code sample.

It provides evidence of my early Flutter experience,
including reactive state management, asynchronous
programming, widget composition, and automated testing.

## Architecture & Implementation

### BLoC-Based State Management

The application uses a BLoC-style approach to separate
asynchronous application state from UI presentation.

The `PlayerBloc` exposes RxDart streams for video controller
state and transcript data.

The UI consumes these streams through Flutter's `StreamBuilder`
widgets.

- [PlayerBloc implementation](https://github.com/YatsenkoDev/chorus/blob/4046baa/lib/bloc/player_bloc.dart)
- [PlayerScreen implementation](https://github.com/YatsenkoDev/chorus/blob/4046baa/lib/screen/player_screen.dart)

The implementation uses a BLoC-style pattern rather than
a fully dependency-injected application architecture.

### State Lifecycle & Resource Management

The player BLoC is created and disposed of through Provider.

Its disposal logic closes RxDart subjects and releases
the video player controller.

- [Provider lifecycle management](https://github.com/YatsenkoDev/chorus/blob/4046baa/lib/screen/player_screen.dart#L17-L20)
- [PlayerBloc resource cleanup](https://github.com/YatsenkoDev/chorus/blob/4046baa/lib/bloc/player_bloc.dart#L62-L66)

### Asynchronous API Integration

The application retrieves transcript data asynchronously
using HTTP requests.

JSON parsing is performed using Flutter's `compute()`,
moving parsing work away from the main isolate.

- [API implementation](https://github.com/YatsenkoDev/chorus/blob/4046baa/lib/api/api_manager.dart)
- [Transcript model](https://github.com/YatsenkoDev/chorus/blob/4046baa/lib/model/transcript.dart)

### Localization

The application configures Flutter localization support
for English, Russian, and Polish.

[View localization configuration](https://github.com/YatsenkoDev/chorus/blob/4046baa/lib/main.dart#L17-L27)

## Automated Testing

The project includes unit, widget, and integration tests
added during its original development in 2019.

### Unit Tests — API & JSON Parsing

[ApiManagerTest](https://github.com/YatsenkoDev/chorus/blob/4046baa/test/api/api_manager_test.dart)

Tests cover:

- Parsing valid transcript JSON.
- Extracting speaker and message information.
- Handling malformed JSON.

[Original unit and widget test commit](https://github.com/YatsenkoDev/chorus/commit/1172667)

### Widget Tests — Screen Behavior

[InsertIdScreenTest](https://github.com/YatsenkoDev/chorus/blob/4046baa/test/screen/inser_id_screen_test.dart)

Verifies screen composition, initial input values,
and validation behavior when an empty ID is submitted.

[PlayerScreenTest](https://github.com/YatsenkoDev/chorus/blob/4046baa/test/screen/player_screen_test.dart)

Verifies screen composition and the initial loading indicator.

### Widget Tests — Component Interactions

[VideoPlayerWidgetTest](https://github.com/YatsenkoDev/chorus/blob/4046baa/test/widget/video_player_widget_test.dart)

Exercises video player widget rendering and
play-button visibility after user interaction.

[TranscriptElementWidgetTest](https://github.com/YatsenkoDev/chorus/blob/4046baa/test/widget/transcript_element_widget_test.dart)

Verifies rendering of single and multiple transcript messages.

### Integration Testing — Flutter Driver

[Original integration test](https://github.com/YatsenkoDev/chorus/blob/4046baa/test_driver/app_test.dart)

The Flutter Driver tests exercise application navigation
and interaction with video playback controls.

They cover user interaction rather than asserting
successful media playback end to end.

[Original integration test commit](https://github.com/YatsenkoDev/chorus/commit/4046baa)

## Historical Context

This project documents the Flutter technologies and
development practices I was using in 2019.

Its architecture and tests reflect the project's original
scope and the Flutter ecosystem at that time.

It is preserved as a historical code sample, not
maintained as a reference for current Flutter best practices.

The original source code and commit history remain unchanged.
