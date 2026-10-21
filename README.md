# Tuition Reader – updates

This repository only hosts update information for the Tuition Reader Android app (a family reading helper).
It contains no source code.

- `version.json` – the **stable** version the kids' phones check (once a day, or Settings › Check for update).
- `version-beta.json` – the **beta** version, read only by phones with Settings › "Beta tester (get new versions first)" switched on.
- APK files are attached to the GitHub Releases on this repository.

## Release process (beta first)

1. A new build is published as a GitHub **pre-release** and only `version-beta.json` is pointed at it.
2. Eric installs it on his own phone (Beta tester switched on) and tests it.
3. Only after Eric's OK is `version.json` changed to point at that same APK, so the kids' phones get it.
4. `version.json` is never changed before step 3.

Every build has a higher `versionCode` and is signed with the same key, so it installs over the previous version.
