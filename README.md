# Expo Linking.getInitialURL() returns null inconsistently on Android

This repository demonstrates a bug in Expo's `Linking` API where `getInitialURL()` inconsistently returns `null` on Android even when a deep link is successfully opened.  This leads to unreliable deep link handling in applications.

The `deepLinkBug.js` file shows the problematic code, while `deepLinkSolution.js` provides a workaround to mitigate the issue.

## Reproducing the bug

1. Clone this repository.
2. Run the app on an Android device or emulator.
3. Open a deep link to the app.
4. Observe that `getInitialURL()` might return `null` in some cases.

## Workaround

The provided workaround involves using a combination of `getInitialURL` and listening for `url` events. This approach improves the reliability of deep link handling.