AURORA IPTV - ANDROID BUILD (needs a PC with Node.js 18+ and Android Studio)

1. Open a terminal in this folder and run:
   npm i @capacitor/core @capacitor/cli @capacitor/android @capacitor/app
   npx cap add android
   npx cap sync android
   npx cap open android

2. In Android Studio:
   - Plug in your phone (USB debugging on) and press Run, or
   - Build > Build APK(s), copy the APK to your phone and install it.

After editing www/index.html, run "npx cap sync android" again.

Why not just open the HTML in a phone browser? Browsers block requests to IPTV servers
(CORS and http/https rules). The Capacitor build uses native networking, so it works.

NO ANDROID STUDIO? BUILD IN THE CLOUD (GitHub)
1. Create a free GitHub account and a new repository.
2. Upload everything in this folder, including the hidden .github folder
   (if it does not upload, use Add file > Create new file, name it
   .github/workflows/build.yml and paste the contents of that file).
3. Open the Actions tab, wait for "Build APK" to finish (about 5 minutes).
4. Open the finished run, download "AuroraIPTV-apk", unzip it, and install app-debug.apk.
