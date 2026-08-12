# Volleyball Team Builder 1.5.1

## Confirmed rules
- Select 1–4 available courts for each session.
- Use a 1.0–10.0 player rating scale in 0.1 increments.
- Teams are 2–5 players; the app prefers the greatest practical number of simultaneous teams allowed by the court count.
- A 2- to 3-player team is guided toward an average about 0.25 above a 4/5-player team, but this is a soft optimization preference rather than a hard rule.
- Published results show teams only—no ratings, averages, or court assignments.

## Recommended free hosting: GitHub Pages
GitHub Pages is the recommended option for this version because the app is a static HTML/CSS/JavaScript site, and Pages publishes a repository as a website with HTTPS. The site files themselves will be public; player ratings and history are not included in the repository because they remain in each device's IndexedDB.

### Publish from a computer
1. Create or sign in to a GitHub account.
2. Create a new public repository named `volleyball-team-builder`.
3. Extract this ZIP.
4. In the repository, choose **Add file > Upload files**.
5. Upload the files from the extracted folder—not the outer folder itself. `index.html` must be at the repository root.
6. Commit the upload.
7. Open **Settings > Pages**.
8. Under **Build and deployment**, choose **Deploy from a branch**.
9. Choose branch **main**, folder **/(root)**, and save.
10. GitHub displays the published site address in the Pages settings. Share that address with the co-organizer.

### Install on iPhone or iPad
1. Open the published HTTPS site in Safari while online.
2. Tap **Share > Add to Home Screen**.
3. Launch the Home Screen app once while online so the files are cached.
4. It can then reopen and operate offline using its device-local data.

## Sharing data with a co-organizer
Hosting shares the app, not the private local roster database. Each device stores its own roster, passcode, settings, and rolling history.

To initialize the co-organizer's copy:
1. On your device, open **Players > Export backup**.
2. Share the downloaded JSON backup through a method you trust.
3. On the co-organizer's device, open the hosted app and use **Players > Import backup**.
4. Each person should set their own device passcode in **Settings**.

Repeat export/import whenever you want to manually align roster changes or history. This version intentionally does not do live multi-device synchronization.

## Why not iCloud Drive?
iCloud Drive can store and share the ZIP or JSON backup, but it is not being used as the web host in this setup. Use iCloud Drive, AirDrop, Messages, or another file-sharing method for backup exchange; use GitHub Pages for the actual HTTPS website.

## Passcode scope
The passcode is a local convenience lock. It is hashed before storage, and backup exports omit it. Because this release has no backend authentication, the hosted app URL is still public and the passcode is not server-grade access control. Do not store sensitive personal information in the app.

## Alternative hosting
Cloudflare Pages is also suitable for static hosting and collaboration, but GitHub Pages is the simpler recommendation for this package because no build step is required.

## Local test
PWA service workers require HTTPS or localhost. From the extracted folder on a computer, run:

    python3 -m http.server 8080

Then browse to `http://localhost:8080` on that computer.
