# FreeVid Studio — open-source Android-friendly starter

A zero-cost, no-API-key browser app designed for Android Chrome. It can be added to the home screen as a PWA when hosted over HTTPS, and its source can be modified freely.

## What works
- Select a reference image from your phone.
- Preview cinematic camera-motion animation (zoom, pan, drift).
- Export a WebM video using the browser's MediaRecorder API.
- Play voiceover text using the device/browser speech synthesis engine.
- Generate and download procedural ambient sound as WAV.
- No accounts, subscriptions, credits, paid APIs, or image uploads.

## Important honesty note
This starter is **not a full generative AI video model**. The video is made by animating the source image with camera movement; it does not invent new frames or change the scene based on the prompt. WAV export is generated ambience, not synthesized speech. Browser/device support varies. Truly realistic on-device image-to-video generation requires bundling a compatible model and inference runtime, which can require many gigabytes of model storage and substantial RAM/GPU/NPU capacity. No free unlimited cloud service is included.

## Run on Android
1. Unzip this folder.
2. Host the files on any static HTTPS host you control (for example, GitHub Pages). No server-side API is required.
3. Open the HTTPS page in Chrome on Android.
4. Use Chrome's menu → **Add to Home screen** / **Install app**.
5. For offline use, open it once while online so the service worker can cache the app shell.

Opening `index.html` directly from a file manager may restrict PWA installation and offline caching. The export buttons require browser support for Canvas captureStream and MediaRecorder.

## Files
- `index.html` — app UI and local image/video/audio processing
- `manifest.webmanifest` — install metadata
- `sw.js` — offline app-shell cache

## License
MIT. You may use, modify, and redistribute this starter. Keep model and asset licenses separate if you add them later.
