WARDROBE 66 — install as an iPhone app
Placeholder & price data for now
======================================

WHAT'S IN HERE
  index.html            the app (also works on its own, offline, from disk)
  manifest.webmanifest  name, icon and full-screen settings
  sw.js                 offline cache
  *.png                 home-screen icons

STEP 1 — PUT THE FOLDER ONLINE (2 minutes, free)

  Option A · Netlify Drop — easiest, no account needed to start
    1. Go to app.netlify.com/drop in any browser.
    2. Drag this whole folder onto the page.
    3. Copy the https://....netlify.app address it gives you.

  Option B · GitHub Pages
    1. Create a repository and upload all files to its root.
    2. Settings > Pages > Source: main branch, / (root). Save.
    3. Wait ~1 minute for the https://yourname.github.io/repo/ address.

  Option C · Cloudflare Pages — same drag-and-drop as Netlify, at
    pages.cloudflare.com. Good if you want a custom domain later.

  It must be https:// — the offline cache will not run over http:// or from
  a file on disk.

STEP 2 — ADD IT TO THE HOME SCREEN

  1. Open the address in SAFARI on the iPhone. Not Chrome — only Safari can
     install to the home screen on iOS.
  2. Tap the Share button (square with an up arrow).
  3. Scroll down and tap "Add to Home Screen".
  4. Name it and tap Add.

  It now launches full screen with no address bar, and works with no signal.

WORTH KNOWING

  * The home-screen app has its OWN storage, separate from Safari. Anything
    you entered while testing in Safari will not appear inside it. Add your
    pieces after installing, or use Export data in Safari and Import data in
    the installed app.
  * iOS can clear a web app's storage if the app goes unused for a long
    stretch, or if the phone is very low on space. Tap "Export data" every
    so often and keep the .json file in Files or iCloud Drive. That file
    restores everything through "Import data".
  * To update the app later, re-upload index.html, bump CACHE = "wardrobe66-v1"
    to "-v2" in sw.js, then close and reopen the app twice.
  * Photos are compressed to roughly 170 KB each. Around 25 photos fit in the
    storage budget; the meter in the add-a-piece screen shows where you are.

NO HOSTING, JUST THIS PHONE?
  Open index.html from the Files app and it still runs — every feature works
  except the home-screen icon and offline cache. Storage may be cleared more
  aggressively, so export often.
