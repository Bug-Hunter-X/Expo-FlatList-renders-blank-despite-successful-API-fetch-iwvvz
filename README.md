# Expo FlatList Blank Render Bug

This repository demonstrates an uncommon bug in Expo where a FlatList component renders blank even after successfully fetching data from an API. The ActivityIndicator displays correctly, indicating the fetch is happening, but the FlatList remains empty.

## Bug Description

The issue occurs when using `FlatList` to render data fetched from an API.  Even with a successful fetch and the data correctly logged to the console, the `FlatList` remains blank. This bug is not consistently reproducible and may be related to specific API responses or timing issues.  There's no explicit error message provided.

## Steps to Reproduce

1. Clone the repository.
2. Install dependencies: `npm install` or `yarn install`.
3. Run the app: `expo start`.
4. Observe that the FlatList displays empty despite the API request succeeding.

## Solution

The solution involves using a `useEffect` hook with `data` as a dependency. This ensures the FlatList re-renders once the data is available.  Additionally, checking for the data's length before rendering further improves the UI behavior.