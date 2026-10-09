# Flutter Open-Source Contributions

Selected contributions to community Flutter packages,
with links to original implementations, upstream discussions,
maintainer reviews, and published release notes.

## Flutter Fortune Wheel — Merged Contribution (2023)

**Package:** [flutter_fortune_wheel](https://pub.dev/packages/flutter_fortune_wheel)

**Status:** Merged and released in version 1.3.0

**[Pull Request #107 — Haptic Feedback & Gesture Physics](https://github.com/kevlatus/flutter_fortune_wheel/pull/107)**

### Implementation

Extended the package with:

- Configurable haptic feedback when the wheel crosses
  section boundaries.
- A configurable gesture physics option controlling
  opposite-direction rotation initiation.

### Independent Review

The pull request was reviewed, approved, and merged
by the package maintainer on July 4, 2023.

**Maintainer feedback:**

> "simple, yet effective implementation of haptic feedback"

The maintainer made a small optimization to the
haptic feedback implementation before merging.

[View the original review and discussion](https://github.com/kevlatus/flutter_fortune_wheel/pull/107)

### Published Release

The haptic feedback functionality was included in
flutter_fortune_wheel 1.3.0, released on July 4, 2023.

The official package changelog explicitly credits
@YatsenkoDev for the contribution.

**[View the official changelog on pub.dev](https://pub.dev/packages/flutter_fortune_wheel/changelog#130---2023-07-04)**

---

### FlutterYoutube — Merged Contribution (2019)

**[Merged PR #53 — Android App Bar Visibility](https://github.com/ponnamkarthik/FlutterYoutube/pull/53)**

Extended a Flutter YouTube player plugin with configurable
Android Action Bar visibility.

The implementation included changes to the public Dart API,
Flutter platform communication, and native Android Java code.

The contribution received positive feedback during code review
and was merged into the upstream repository in December 2019.

**Reviewer feedback:**
> "Perfect."

[View the original review and merged implementation](https://github.com/ponnamkarthik/FlutterYoutube/pull/53)

---

## Flutter Health Plugin — Cross-Platform Extension (2024)

**Project:** [CACHET Flutter Plugins](https://github.com/carp-dk/flutter-plugins)

**Implementation:** [Public fork](https://github.com/YatsenkoDev/flutter-plugins)

### Motivation

Health data collected from different devices and sources
can contain overlapping measurement intervals.

Simply summing individual health records may therefore
produce totals that differ from native health applications.

The implementation extends the existing Flutter health
plugin with native aggregation functionality.

### Implementation

Added two methods:

- `getTotalCaloriesInInterval`
- `getTotalDistanceInInterval`

Implemented the functionality on both Android and iOS,
using their respective native health APIs.

### Original Implementation History

- [Android implementation — February 14, 2024](https://github.com/YatsenkoDev/flutter-plugins/commit/2109de07dab4a1fb4516dee1b18becceeba1e3eb)
- [iOS implementation — February 14, 2024](https://github.com/YatsenkoDev/flutter-plugins/commit/dd79d909fd969db7b40b548a6e0836b6a13558e3)
- [Cross-platform unit consistency](https://github.com/YatsenkoDev/flutter-plugins/commit/a88ab838b0eed62d36790074e066ad7a0bef4b1c)
- [Android aggregation corrections — March 2, 2024](https://github.com/YatsenkoDev/flutter-plugins/commit/08b414f8e9b4437fad3d0ec6175789cfde8a7436)

### Upstream Discussion

The motivation and proposed functionality were also
discussed in the upstream project's issue tracker.

[View upstream issue #177](https://github.com/carp-dk/carp-health-flutter/issues/177)

The implementation is available in the public fork.
