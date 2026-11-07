# manga-reader-live — OTA live bundles for Manga Reader ID

Release assets ONLY. No source code, no secrets.

- Each `live` release holds one web bundle (`live-bundle-vNNN.zip`) + its
  signed manifest (`live-update.json`) for the Manga Reader ID Android app
  (DIY OTA, one channel per APK `versionCode`).
- The manifest carries version, zip URL, SHA-256, RSA signature, and
  min/max APK build. The app verifies the signature + SHA-256 BEFORE
  applying a bundle, and rolls back if the bundle never marks itself OK.
- The bundle is the same web app already served publicly by the Vercel
  frontend — it contains no secret (admin secret was removed from the
  frontend in v10; the app authenticates with a session token).
- Do NOT install these zips manually. The app fetches and applies them itself.
