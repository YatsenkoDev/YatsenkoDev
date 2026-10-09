# Transformer Arena — Android Engineering (2018)

**Java · Android · MVP · Dagger · RxJava · Retrofit · JUnit · Mockito · Espresso**

[Original repository](https://github.com/YatsenkoDev/Transformer-Arena) |
[Original 2018 source snapshot](https://github.com/YatsenkoDev/Transformer-Arena/tree/b1de7133b29cdf1a09595f728fd227fd7256c4ef) |
[2018 unit-test commit](https://github.com/YatsenkoDev/Transformer-Arena/commit/b1de7133b29cdf1a09595f728fd227fd7256c4ef)

## Project Context

A native Android application developed in 2018 as a coding assignment.

The application manages Transformer characters, supports creating
and editing them through a REST API, and calculates battles between teams.

This repository is preserved in its original state.

Its value as a historical code sample is the opportunity to examine
the architecture, dependency management, asynchronous programming,
and testing practices I was using in 2018.

## Architecture & Implementation

### MVP-style Architecture

The application separates screen presentation from service-level
operations using dedicated presenters, view interfaces, and services.

Examples:

- [GalleryPresenter](https://github.com/YatsenkoDev/Transformer-Arena/blob/b1de7133b29cdf1a09595f728fd227fd7256c4ef/app/src/main/java/com/aequilibrium/assignment/transfarena/gallery/presenter/GalleryPresenter.java)
- [PreviewPresenter](https://github.com/YatsenkoDev/Transformer-Arena/blob/b1de7133b29cdf1a09595f728fd227fd7256c4ef/app/src/main/java/com/aequilibrium/assignment/transfarena/preview/presenter/PreviewPresenter.java)
- [TransformersLoadingService](https://github.com/YatsenkoDev/Transformer-Arena/blob/b1de7133b29cdf1a09595f728fd227fd7256c4ef/app/src/main/java/com/aequilibrium/assignment/transfarena/gallery/service/TransformersLoadingService.java)

This is an MVP-style implementation rather than a strict
framework-independent presentation layer.

### Dependency Injection

Presenters and services receive dependencies through constructors
annotated with `@Inject`.

This makes dependencies explicit and enables unit tests to instantiate
components with mocked collaborators.

[Example: PreviewPresenter constructor injection](https://github.com/YatsenkoDev/Transformer-Arena/blob/b1de7133b29cdf1a09595f728fd227fd7256c4ef/app/src/main/java/com/aequilibrium/assignment/transfarena/preview/presenter/PreviewPresenter.java#L40-L46)

### Reactive & Asynchronous Operations

RxJava is used for asynchronous API requests and battle calculations,
with explicit scheduling between background execution and the UI thread.

The implementation also includes disposal of active subscriptions
during screen lifecycle transitions.

- [REST API loading and subscription disposal](https://github.com/YatsenkoDev/Transformer-Arena/blob/b1de7133b29cdf1a09595f728fd227fd7256c4ef/app/src/main/java/com/aequilibrium/assignment/transfarena/gallery/service/TransformersLoadingService.java)
- [Asynchronous battle calculations](https://github.com/YatsenkoDev/Transformer-Arena/blob/b1de7133b29cdf1a09595f728fd227fd7256c4ef/app/src/main/java/com/aequilibrium/assignment/transfarena/battle/service/BattleService.java)

## Automated Testing

The original October 2018 commit introduced eight additional
JUnit/Mockito test files covering presenters, services, and utilities.

**[View the original test commit — October 2018](https://github.com/YatsenkoDev/Transformer-Arena/commit/b1de7133b29cdf1a09595f728fd227fd7256c4ef)**

Selected examples:

### Validation & Preventing Unwanted Side Effects

[PreviewPresenterTest](https://github.com/YatsenkoDev/Transformer-Arena/blob/b1de7133b29cdf1a09595f728fd227fd7256c4ef/app/src/test/java/com/aequilibrium/assignment/transfarena/preview/presenter/PreviewPresenterTest.java#L49-L66)

Verifies that an empty name produces a validation error
without invoking create or update operations.

### Lifecycle & Resource Cleanup

[GalleryPresenterTest](https://github.com/YatsenkoDev/Transformer-Arena/blob/b1de7133b29cdf1a09595f728fd227fd7256c4ef/app/src/test/java/com/aequilibrium/assignment/transfarena/gallery/presenter/GalleryPresenterTest.java#L43-L55)

Verifies that destroying the view interrupts the loading
service and disposes of the event subscription.

### Conditional Business Logic

[BattlePresenterTest](https://github.com/YatsenkoDev/Transformer-Arena/blob/b1de7133b29cdf1a09595f728fd227fd7256c4ef/app/src/test/java/com/aequilibrium/assignment/transfarena/battle/presenter/BattlePresenterTest.java#L52-L79)

Checks both the valid battle-start path and rejection of
an attempt to start a battle with empty teams.

## Historical Context

This project is a preserved example of my Android development
work from 2018, not a maintained application or a reference
implementation of current Android best practices.

The original source code and commit history remain unchanged.
