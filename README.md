# Silent Image Loading Failure in Expo Image Component

This repository demonstrates a subtle bug in Expo's `Image` component where image loading fails silently.  No error messages are logged to the console, making debugging difficult. The problem is intermittent, and the cause is not always obvious.

## Problem Description

The `Image` component sometimes fails to load images without providing any error feedback. This leads to unexpected visual glitches in the app, where an image placeholder remains or nothing appears.

## Solution

The provided solution adds robust error handling using a custom `Image` component with a `onError` prop. This allows us to catch loading failures and display a fallback image or message.  It's crucial to handle network errors and invalid image URIs for a reliable user experience.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `expo start` to start the Expo development server.
4. Observe the image loading behavior. Some images may load successfully, while others might not, without error messages.

## Technologies Used

* Expo
* React Native
* JavaScript