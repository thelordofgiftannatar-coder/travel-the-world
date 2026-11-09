# Gotham Gazette

Gotham Gazette is an Android-first AI image studio packaged in the existing Android WebView shell.

## Features
- Gemini 3.1 Flash Image and Gemini 3 Pro Image support.
- 1K, 2K and 4K Gemini image-size options, subject to model/API availability.
- Reference-image editing and remixing with Gemini.
- Optional OpenAI Images API provider.
- Local IndexedDB gallery, downloads and prompt reuse.
- Prompt enhancement for photorealistic, cinematic results.

## Build the Android APK with GitHub Actions
1. Push this repository to GitHub.
2. Open **Actions → Build Gotham Gazette Android APK**.
3. Run the workflow (or push to `main` / `master`).
4. Download the `Gotham-Gazette-Android-APK` artifact from the completed workflow.

The APK is signed with an ephemeral CI key. Each build has a different signing identity, so install it as a fresh app rather than expecting an update over an APK signed by a different key.

## Configure image generation
Open **API settings** inside the app and add your own Gemini API key. Create one at https://aistudio.google.com/app/apikey. The key is stored locally on that device. Do not put API keys in this repository or commit them to GitHub.

Gemini image generation can produce 1K, 2K and 4K images with supported Gemini 3 image models. Availability, speed, quotas and charges depend on your Google account and API plan. This app does not provide unlimited free generations.

## Privacy
Prompts and optional reference images are sent to the selected AI provider for processing. Generated images are stored locally on the device in IndexedDB. API keys are stored in the app's local browser storage. Avoid using a shared or untrusted device.
