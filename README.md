# CH GTA AI CLIPPER — Mobile Browser Edition

## What this build does
- Mobile-first browser interface (PWA-ready).
- Select a video stored on your phone.
- Review evenly spaced clip suggestions and edit start/end timestamps.
- Export selected clips as MP4 using FFmpeg.wasm in the browser.
- Portrait 9:16, square 1:1, or landscape 16:9 output.
- 720p or 1080p, Gaming/Podcast/Interview/Tutorial/Vlog labels, blurred background or crop layout.
- The source video is processed in the browser; it is not uploaded to this app's server.

## Important honest limitations
- This first mobile build does NOT perform semantic AI highlight detection. Suggestions are evenly spaced timestamps.
- Automatic speech recognition, Hindi/Hinglish transcription, burned-in captions, SRT generation, ZIP export, background jobs, and reliable 5–6 hour processing are not implemented in this mobile build.
- FFmpeg.wasm needs an internet connection on first load to fetch its open-source engine. Large videos may fail due to Android browser memory limits. Start with a short 20–60 second test video and 720p.
- Keep the browser tab open during export. Do not lock the phone.
- Use only footage you own or have permission to edit. A public video URL alone is not permission to download or repost it.
- This is a browser app source package, not a hosted public website. Deploy the files to a static HTTPS host (e.g. GitHub Pages or Vercel) to open it in Chrome. Do not expose a local development server to the public internet.

## Local test
Serve this folder over HTTPS or localhost. For desktop testing:
`python -m http.server 8000`
Then open `http://127.0.0.1:8000`. On Android, localhost on a different device will not work; deploy to an HTTPS static host.

## Deploy
Upload `index.html`, `manifest.webmanifest`, and `sw.js` to a static hosting provider. Ensure the site is served over HTTPS. The FFmpeg engine is loaded from public CDNs at runtime.
