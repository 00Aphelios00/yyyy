# FRIDAY MAVI for Android (source project)

This is a native Android Java app, not an APK. It includes a blue MAVI UI, Android TTS, Android speech recognizer, local commands, optional Groq AI API connection, and an opt-in Accessibility service for Home/Back/visible text clicks. This code has not been compiled or tested on a device in this environment.

## Building in GitHub
1. Create a PRIVATE GitHub repository. You can initialize it empty.
2. Upload ALL the files and folders from this archive **at the repository root**, including `.github/workflows/android.yml` (do NOT upload the ZIP as one blob). GitHub's web uploader can make folder uploads difficult; using GitHub Desktop or `git` from a PC is more reliable.
3. Open the `Actions` tab, choose **Build FRIDAY MAVI Android APK**, click **Run workflow**.
4. If the run succeeds, open the run and download **FRIDAY-MAVI-debug-APK** from Artifacts. Extract to find `app-debug.apk`.

## Notes
- Voice recognition uses Android's built-in recognition intent and may require internet and a supported speech service. TTS voices depend on your Android installation; no exact movie actor voice is provided.
- Optional AI mode uses `https://api.groq.com/openai/v1`, model `openai/gpt-oss-20b`. No key is needed for Local mode.
- The API key is stored in app-private local preferences, not a secure server vault. Don't publish a key or embed one in a public repository.
- Accessibility service must be manually enabled in Settings > Accessibility > FRIDAY Screen Control. It is opt-in and supports Home, Back and click by visible text. Other apps' controls may not expose accessible text; control is not guaranteed.
- APK is a debug build and has NOT been compiled here. No background always-listening functionality.
