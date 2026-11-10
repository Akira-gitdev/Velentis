# Velentis

One app with many small tools, by Flamebounds. This folder turns it into an Android app (an APK) using GitHub. You do everything from your phone's browser. No laptop needed.

## What is in here

| File | What it does |
| --- | --- |
| `VELENTIS-index.html` | The app itself: home screen, habit tracker, and the nine looks |
| `VELENTIS-intro.html` | The opening logo animation |
| `package.json` (keeps its name) | The list of tools the build needs |
| `capacitor.config.json` (keeps its name) | The app's name and ID |
| `VELENTIS-make-assets.mjs` | Draws the app icon and start screen for you |
| `VELENTIS-build-apk.yml` | The recipe GitHub follows to build the APK |

## Steps

1. **Make a repository.** Open github.com in your browser and sign in. Tap **+** at the top, then **New repository**. Name it `velentis` and tap **Create repository**.
2. **Upload the files.** On the new repository page, tap **uploading an existing file** (or **Add file**, then **Upload files**). Pick all six files from the list above, including `VELENTIS-build-apk.yml`. Tap **Commit changes**.
3. **Move the recipe into place.** GitHub only reads the recipe from a special folder.
   - Tap `VELENTIS-build-apk.yml` in the file list, then the pencil icon (**Edit**).
   - At the top, tap the file name box. Delete the old name and type exactly `.github/workflows/VELENTIS-build-apk.yml`
   - Tap **Commit changes**.
4. **Start the build.** The build starts by itself after that commit. To start it by hand, open the **Actions** tab, tap **Build Android APK**, then **Run workflow**. It takes about 10 minutes the first time.
5. **Download the app.** When the run shows a green tick, go back to the main page of the repository and tap **Releases** on the right. Open the newest build and tap **Velentis.apk** to download it.
6. **Install it.** Open the downloaded file. Android will ask you to allow installs from your browser. Allow it, then tap **Install**. A warning that the app is from an unknown developer is normal for apps you build yourself.

## Good to know

- The first time the app opens, it needs the internet to load its fonts. After that it works with whatever fonts are saved on your phone.
- Your habits and your chosen look are saved on your phone only. Clearing the app's data erases them.
- This is a test build for your own phone. It is not ready for the Play Store.

## If the build fails

Open the **Actions** tab, tap the run with the red cross, and tap the step that has the red cross. Copy the last few lines of text and send them to Claude. It will tell you what to change.
