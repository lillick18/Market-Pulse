# Market Pulse (Samsung A54 install guide)

This build is a Progressive Web App. It runs fully on the phone, works offline after the first load, and installs with its own icon. It still uses SIMULATED prices and cannot place orders.

## Install on the A54 (about 5 minutes, no coding)
1. Put the `www` folder on any free static host that gives you an https link, for example Netlify Drop (app.netlify.com/drop, drag the folder in) or GitHub Pages.
2. On the phone, open that link in Chrome.
3. Tap the menu (three dots), then "Add to Home screen" (or "Install app"). Open Market Pulse from the home screen.

## Build a real APK instead (needs a PC with Node 18+, Java 17 and Android Studio)
    npm install
    npx cap add android
    npx cap sync android
    npx cap open android        # then Build > Build APK(s) in Android Studio
Copy the APK to the phone and allow installs from your file manager when asked.

## Going live with real data
See `backend/README.md`. Run the backtest on real candle files first, then fill in the broker adapters. Orders are intentionally not implemented, and signals are not advice.
