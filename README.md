# Gem Rush – offline Android game

Single-file HTML5 game (`index.html`). No internet, no libraries, no asset files: graphics are drawn in code and sounds are generated on the fly, so it works 100% offline.

## Play it right now
Open `index.html` in any browser (Chrome on a phone works great). Controls: drag a finger / mouse, or ← → keys. `P` pauses.

## Turn it into an APK (about 10 minutes)

You need: Node.js 18+ and Android Studio (or just the Android SDK + JDK 17).

```bash
npm install
npm run android:add        # one time: creates the android/ project
npm run android:apk        # builds the debug APK
```

Your APK is at:
`android/app/build/outputs/apk/debug/app-debug.apk`

Copy it to your phone and tap it to install (allow "install unknown apps" if asked).

Prefer clicking? After `npm run android:add`, run `npx cap open android`, then in Android Studio choose **Build → Build APK(s)**.

### Even easier, no coding
Zip `index.html` and use an HTML-to-APK service (e.g. "WebIntoApp", "Appsgeyser"). Check that the option you pick bundles the files inside the app (offline), not a link to a website.

### Play Store release
Use **Build → Generate Signed Bundle / APK** in Android Studio and sign with your own keystore.

## Game features
- Catch gems and stars, dodge bombs, chain combos (up to x5)
- Power-ups: shield, magnet, slow-mo, extra heart
- Levels get faster as you score; background changes color each level
- Pause, sound and vibration toggles, saved high score, built-in how-to-play
- Auto-pauses when you switch apps
