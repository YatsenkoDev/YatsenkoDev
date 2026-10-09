# Instagram Preview — Flutter Engineering (2019–2020)

**Flutter · Dart · Provider · RxDart · Hive · REST API · Drag-and-Drop**

[Original repository](https://github.com/YatsenkoDev/Instagram-preview) |
[Original 2020 source snapshot](https://github.com/YatsenkoDev/Instagram-preview/tree/6d36074439d7b89f627eb86ffac8bd425819d6bc) |
[Drag-and-drop implementation commit](https://github.com/YatsenkoDev/Instagram-preview/commit/af7f245810dd85124a9b27ddc35be7e94a4ed500)

## Project Context

A Flutter application developed during 2019–2020
for previewing and rearranging Instagram photos.

The application integrates with the Instagram API,
supports account selection, retrieves media, and
allows users to rearrange photos in a grid.

This repository is preserved as a historical code sample
of my early Flutter application development.

## Architecture & Implementation

### Reactive State Management

The application uses BLoC-style state management
with RxDart `BehaviorSubject` streams and Provider.

Separate components manage account selection,
photo collections, and the photo grid.

- [HomeBloc](https://github.com/YatsenkoDev/Instagram-preview/blob/6d36074439d7b89f627eb86ffac8bd425819d6bc/lib/feature/home/bloc/home_bloc.dart)
- [FeedBloc](https://github.com/YatsenkoDev/Instagram-preview/blob/6d36074439d7b89f627eb86ffac8bd425819d6bc/lib/feature/home/bloc/feed_bloc.dart)
- [HomeScreen](https://github.com/YatsenkoDev/Instagram-preview/blob/6d36074439d7b89f627eb86ffac8bd425819d6bc/lib/feature/home/screen/home_screen.dart)

The implementation separates much of the asynchronous
state handling from widget rendering, although it does
not provide complete dependency isolation.

### Interactive Photo Reordering

The photo grid supports long-press drag-and-drop
reordering using Flutter's `LongPressDraggable`
and `DragTarget` widgets.

The interaction coordinates UI events with
reactive state updates and local persistence.

Key implementations:

- [FeedElement — drag-and-drop UI](https://github.com/YatsenkoDev/Instagram-preview/blob/6d36074439d7b89f627eb86ffac8bd425819d6bc/lib/feature/home/widget/feed_element.dart)
- [FeedBloc — photo reordering](https://github.com/YatsenkoDev/Instagram-preview/blob/6d36074439d7b89f627eb86ffac8bd425819d6bc/lib/feature/home/bloc/feed_bloc.dart)
- [PhotoElement — immutable-style state updates](https://github.com/YatsenkoDev/Instagram-preview/blob/6d36074439d7b89f627eb86ffac8bd425819d6bc/lib/feature/home/model/photo_element.dart)

**[Original feature commit — January 20, 2020](https://github.com/YatsenkoDev/Instagram-preview/commit/af7f245810dd85124a9b27ddc35be7e94a4ed500)**

This commit provides a historical record of
the implementation during its original development.

### API Integration

The application integrates with Instagram's
authentication and media APIs.

It includes asynchronous HTTP requests,
token handling, and media response parsing.

The media parsing implementation uses Flutter's
`compute()` to process JSON outside the main isolate.

[View API implementation](https://github.com/YatsenkoDev/Instagram-preview/blob/6d36074439d7b89f627eb86ffac8bd425819d6bc/lib/api/api_manager.dart)

### Local Persistence

Hive is used to store application data, including:

- Previously selected accounts.
- User information.
- Retrieved photo URLs.
- User-defined photo ordering.

[View RepositoryManager](https://github.com/YatsenkoDev/Instagram-preview/blob/6d36074439d7b89f627eb86ffac8bd425819d6bc/lib/repository/repository_manager.dart)

### Localization

The application includes English and Russian
localization support.

[View localization configuration](https://github.com/YatsenkoDev/Instagram-preview/blob/6d36074439d7b89f627eb86ffac8bd425819d6bc/lib/main.dart)

## Historical Context

This application documents my practical Flutter
development experience from 2019–2020.

It demonstrates early work with reactive state management,
API integration, local storage, and interactive UI features.

The original implementation has limitations in dependency
isolation, error handling, and automated test coverage.

It is preserved as a historical code sample rather than
a reference implementation of current Flutter practices.

The original source code and commit history remain unchanged.
