VOLLEYBALL TEAM BUILDER - VERSION 1.3.1 DIRECT PACKAGE

This is a clean full ZIP package based on the Version 1.3 feature set, with the passcode compatibility and version-label fixes included directly. It is not an updater script.

What to upload
- Extract this ZIP.
- Upload all extracted files to the root of the existing GitHub Pages repository.
- Ensure index.html, app.js, styles.css, sw.js, manifest.json, icon.svg, README.txt, CHANGELOG.txt, and .nojekyll are all replaced.

Before updating
- In the currently working app, use Players > Export backup.

After updating
- Open the GitHub Pages site in normal Safari while online.
- Confirm the header reads Version 1.3.1.
- Use the existing passcode. This build accepts both historical passcode hash formats and normalizes a legacy match.
- If the Home Screen app still shows stale content, open the normal Safari page online first. Only clear website data after exporting a backup.

Data preservation
- The IndexedDB database name remains volley-builder.
- The state key remains app.
- Roster, calculation settings, team history, player ratings, designations, and tags are preserved for the same site origin.
