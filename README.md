# My Favorite Quotes

My Favorite Quotes is a native Android app for keeping a personal quote collection. Add a line you want to remember, record who said it, and choose one quote as your current favorite. The collection stays on your device and can be read offline.

## What you can do

- Add a quote and its author, browse saved entries, and delete individual quotes.
- Pick a favorite and see it in Settings. Choosing a new favorite replaces the previous one.
- Fetch a random quote from API Ninjas and decide whether to save it alongside your own entries.
- Switch between light and dark mode and export the collection as text.

## How it works

The app uses Kotlin, XML layouts, and Android Fragments. Each screen has a ViewModel that handles its actions. When you save a quote from the API, Retrofit retrieves the quote, the repository writes it to Room, and the collection screen observes the updated list. Preferences DataStore remembers the theme and the selected favorite between sessions.

## Run locally

1. Clone this repository and open its root folder in Android Studio.
2. Select JDK 17 for Gradle, install Android SDK Platform 35, and sync the project.
3. To enable random quotes, add the following line to the project's `local.properties` file, substituting your own API Ninjas key. You can skip this step to use the local collection.

   ```properties
   API_NINJAS_KEY=your_api_ninjas_key
   ```

4. Run the `app` configuration on an emulator or device with Android 7.0 (API 24) or later.
