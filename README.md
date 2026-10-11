# My FPPR v1.0 — Android project

Offline-first prototype for forest patrol recording. Package: `com.kfs.myfppr`. Prototype username: `Kibes` (the password field is not enforced in this demo).

## Features in this prototype
- Offline patrol records stored locally on the phone
- Officer, forest/station, area, observation, action, tree species and wildlife fields
- GPS capture using the last known device location
- Camera thumbnail saved locally with the next patrol record
- Patrol history and CSV export/share workflow

## Build APK in the cloud (no Android SDK on your phone)
1. Create a GitHub account and a **new public repository** named `MyFPPR` at https://github.com/new.
2. On the repository page, choose **Add file → Upload files**. Extract this ZIP first, then upload the *contents* of the `MyFPPR` folder, including the hidden `.github` folder. If uploading from a phone, enable “show hidden files” in the file picker if needed.
3. Commit the uploaded files to the `main` branch. GitHub Actions will automatically run the build.
4. Open the repository's **Actions** tab, select **Build My FPPR APK**, and open the latest successful run.
5. Under **Artifacts**, download `My-FPPR-v1.0-APK`. Extract it to get `app-debug.apk`.
6. On your Infinix, tap the APK and allow installation from your browser/files app when Android asks.

GitHub Actions uses a cloud runner with Java and Gradle; the Android Gradle plugin downloads required Android dependencies during the build. The generated debug APK is suitable for personal testing, not a Play Store release.

## Important prototype limitations
- This is a prototype, not an officially approved Kenya Forest Service system. Do not store sensitive operational data until it has been reviewed and authorized.
- GPS uses the device's last known location; go outdoors and enable Location for best results.
- Camera integration saves the camera thumbnail rather than full-resolution output.
- CSV export currently shares the saved export location; it is not a polished document-management workflow.
- Login is a prototype gate, not secure authentication.
