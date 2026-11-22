# Rua Agora

A free Android app that shows the name of the street you are on in a home screen widget and speaks only the street name when it changes.

## How it works

- The phone's GPS gives the position.
- The street name comes from Android's built-in address service. If it is not available, the app falls back to OpenStreetMap Nominatim (light, personal use).
- A foreground service with a permanent notification keeps tracking on. Android requires this notification.
- The widget shows the current street. Tapping it opens the app.
- Speech uses the phone's own text-to-speech voice, in Brazilian Portuguese.

## How to build and install (GitHub, nothing to install)

1. Create a free account at github.com and a new repository.
2. Upload every file in this folder, including the hidden `.github` folder.
3. Open the **Actions** tab, choose **Build APK** and press **Run workflow**.
4. When it shows a green check, open the run and download the artifact **rua-agora-apk** at the bottom.
5. Unzip it and install `app-debug.apk` on the phone (allow installs from unknown sources when asked).

## How to use

1. Open the app, tap Start and allow precise location and notifications.
2. Long-press an empty spot on the home screen, tap Widgets and choose Rua Agora.
3. To stop, tap Stop in the app or in the notification.

## Privacy and battery

- The position is used only to find the street. Android sends the coordinates to its address service or, on the fallback, to OpenStreetMap Nominatim. This app has no server and stores nothing.
- Keeping GPS on all the time drains the battery. Stop it when you do not need it.

## Limits

- The widget only updates while tracking is on.
- On roads or places without a named street, the app keeps the last street.
- If the phone has no Brazilian Portuguese voice installed, the app shows the street but does not speak it.
- This project was not compiled or tested on a device by its author. If the first build fails, send the error message.
