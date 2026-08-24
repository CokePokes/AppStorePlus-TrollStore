# AppStorePlus-TrollStore
AppStore++ tweak for TrollStore

Allows you to downgrade installed apps.

How to install: 
1. Install TrollStore on your device: https://github.com/opa334/TrollStore
2. Download AppStore++ [here](https://github.com/CokePokes/AppStorePlus-TrollStore/releases/download/v2.2.1-2/AppStorePlus-v2.2.1-2.tipa) from your mobile safari.
3. Open Files app and "Open in" Trollstore. & Done.

Enjoy. 

Changes: 

# What’s New in 2.2.14-1

## On-device Apple Account support

- AppStore++ can now use the Apple Account already signed into the device for silent version lookups and account-authorized IPA downloads.
- Most account-based features no longer require a separate Apple Account login inside AppStore++.
- The separate AppStore++ login is now marked as deprecated.
- Added a setting to disable use of the saved AppStore++ login without deleting the saved session.
- Settings now displays the current on-device Apple Account as read-only information.
- Existing saved AppStore++ sessions remain available for fallback use.

## Version lookup and download queue

- Integrated silent device-account version enumeration into normal version lookups.
- Added pause and resume support for queued version lookups.
- Version results are now cached as each version resolves, allowing interrupted jobs to continue without starting over.
- Improved Round Robin processing so multiple queued apps perform real work on each turn.
- Removed the unnecessary delay between Round Robin turns.
- Moved the Round Robin preference into its own Downloads section in Settings.
- Fixed cancelling one queued app incorrectly cancelling the next app.
- Fixed queued apps appearing to alternate without downloading any version metadata.
- Fixed queue progress being assigned to the wrong app.
- Fixed cancelled lookups failing to display successfully resolved partial results.
- Fixed progress indicators not updating during device-account lookups.
- Stops lookup at unsupported legacy architecture boundaries instead of continuing through unusable builds.

## IPA downloads and library

- Added silent, account-authorized IPA downloading through the on-device Apple Account.
- Connected device-account IPA downloads to the existing download manager.
- Redesigned the IPA Library to group multiple downloaded versions under a single app entry.
- Added a dedicated per-app screen showing every saved IPA version.
- Added search to the IPA Library.
- Improved IPA name, version, build, and icon recovery by reading metadata directly from the archive.
- Fixed icons from unrelated apps being assigned to downloaded IPAs.
- Added an IPA installation-method preference with **MobileInstallation** and **TrollStore** options.
- TrollStore installs now hand the selected local IPA directly to TrollStore for import.
- AppStore++ verifies that TrollStore is actually registered to handle the file before opening it.
- Added clear fallback instructions when TrollStore is installed but is not registered to receive IPA files.
- Added separate **Restore Backup** and **Install + Restore Backup** actions.

## AppStore++ updates and TrollStore

- Improved AppStore++ update installation through TrollStore.
- Downloaded `.tipa` update files are passed directly to TrollStore instead of relying only on the optional URL-scheme setting.
- AppStore++ now detects whether `apple-magnifier://` belongs to TrollStore or Apple’s Magnifier app.
- Prevents update attempts from accidentally opening Magnifier when TrollStore’s URL scheme is disabled.
- Added clearer errors when TrollStore is missing, cannot accept the update file, or needs to be opened once to register its file handlers.

## Installed apps and backups

- Added **Clear All App Data** to the installed-app action menu, including accessible Keychain data, with destructive confirmation.
- Added a first-run tutorial explaining that users can hold an installed app to reveal download and management options.
- Improved the tutorial layout for different screen sizes and dark mode.

## Settings and support

- Added a dedicated Downloads section for queue preferences.
- Added a Cash App donation button under Support.
- Support email now requires a user-entered problem description, preventing empty emails containing only logs or an automatic signature.
- Settings now displays the complete AppStore++ marketing version and build number in its footer.

## Fixes and refinements

- Improved queue state isolation when multiple apps are downloading versions.
- Improved partial-result persistence and cache recovery after cancellation.
- Fixed several IPA artwork and metadata mismatches.
- Improved long-press guidance and action-sheet usability.

---

Thank you to everyone who submitted logs, tested builds, and reported issues.

# AppStore++ 2.2.8-2 Changelog

- Fixed some of the OPEN buttons not working correctly
- Version fix


# AppStore++ 2.2.8-1 Changelog

This is one of the largest AppStore++ updates yet, bringing major improvements to version management, account integration, downloads, backups, and the overall interface.

## New App Store experience

- Added a redesigned App Store-style search interface.
- Search results now include app icons, screenshots, developer information, categories, ratings, and compatibility details.
- Added full app-detail pages with:
  - Promotional header artwork when available
  - Screenshots and previews
  - Ratings and written reviews
  - Age rating, category, developer, language, size, and compatibility information
  - What's New and Version History sections
  - Installed, purchased, and download status
- Installed apps can now open directly into their AppStore++ details page.

## Purchased apps

- Added a Purchased Apps browser.
- Browse:
  - All purchased apps
  - Apps not currently installed
  - Removed or delisted apps still associated with your account
- Added search and compatibility information.
- Added App Store-style cloud download, GET, and MANAGE buttons.
- Improved artwork recovery for removed and uninstalled apps.
- Added a signed-out state that prevents unusable purchased-app results from being displayed.

## Apple Account support

- Added Apple Account login within AppStore++.
- Store sessions are securely saved in the device Keychain.
- Improved two-factor authentication handling.
- Improved commerce-pod redirect and login-response handling.
- Added automatic saved-session validation.
- Expired sessions are detected and safely removed.
- Logged-in sessions can enumerate versions without triggering Apple's compatibility-download prompt in many cases.

## Version browser

- Replaced the large legacy alert with a dedicated, searchable version chooser.
- Added favorite and pinned versions.
- Favorites appear in their own section above the complete version list.
- The currently installed version is clearly identified.
- Added device compatibility information where available.
- Cancelled or unresolved versions are no longer shown as misleading build entries.
- Improved large-list performance and added a "Preparing Results" progress display.
- Added cancellation and background continuation controls.

## Download queue

- Added a proper multi-app version lookup and download queue.
- Added two scheduling modes:
  - Round Robin, which alternates requests between queued apps
  - Finish App First, which completes one app before starting the next
- Added a compact global download banner with overall progress.
- The banner can be collapsed into a side indicator.
- Added per-app icons and progress information.
- Reduced unnecessary list refreshing and UI movement.
- Version lookup completion notifications now include the app's name.

## IPA Library

- Added an IPA Library for saved and exported app versions.
- Displays the app name, icon, version, build, file size, and associated backup count.
- Added direct IPA installation through iOS installation services.
- Added support for account-authorized App Store IPA packages.
- Added delete controls.
- Added upgrade and downgrade version lookup from the IPA Library.
- Added improved metadata and icon recovery directly from IPA contents.
- Added installation progress and completion notifications.

## IPA exporting

- Added exporting of selected App Store versions as IPA files.
- Added progress reporting and cancellation.
- Exported IPAs are automatically added to the IPA Library.
- Improved package reconstruction, executable permissions, metadata, and App Store authorization data.
- Added support for queued IPA downloads.

## App-data backups

- Added per-version app-data backups from the Installed Apps screen.
- Backups now include:
  - App version and build information
  - Backup date
  - Compressed size
  - App icon and display name
- Backups are compressed to save storage space.
- Added optional restoration of portable Keychain items where accessible.
- Keychain backup data is encrypted using a device-protected key stored in the Keychain.
- Added restore and delete controls.
- Apps are closed automatically before restoring their data.
- Added a browser showing every app with available backups.
- Added dedicated per-app backup history pages.

## Installed apps

- Added App Store-style app launch controls.
- Added confirmation before launching an app.
- Added Delete App with a destructive confirmation and completion notification.
- Added Delete Cached Versions.
- Added app-data backup and backup-management actions.
- Improved installed-version detection.
- Added a custom pull-out alphabetical index for navigating large app libraries.

## Notifications

- Version lookup notifications now identify the relevant app.
- IPA download and installation operations now report progress and completion.
- Tapping a successful installation notification can open the newly installed app.
- Added clearer compatibility and installation failure notifications.

## Logging and support

- Added optional AppStore++ logging.
- Added advanced iOS system logging for supported TrollStore installations.
- Logs reset when AppStore++ starts.
- Added compressed log attachments to reduce email size.
- Added a progress indicator while preparing support attachments.
- Added Contact Support with logs attached automatically.

## Interface improvements

- Added a redesigned navigation pill for moving between AppStore++ sections.
- Added a dedicated IPA Library page.
- Improved transitions and animations throughout the app.
- Added App Store-style icons, buttons, placeholders, cells, and progress indicators.
- Improved iPad action-sheet presentation.
- Improved empty states and signed-out messages.
- Reduced lag when opening large version lists and the IPA Library.
- Fixed cell flashing and unstable animations while downloads are active.

## Fixes and improvements

- Improved App Store version enumeration and caching.
- Improved storefront-aware purchases for apps unavailable in the US storefront.
- Improved redownload handling for removed apps.
- Improved pricing-parameter selection and fallback behavior.
- Fixed multiple compatibility-download prompts continuing after cancellation.
- Fixed missing or incorrect icons in download and IPA lists.
- Fixed several Apple login, 2FA, redirect, and session-persistence issues.
- Fixed IPA extraction and installation failures.
- Fixed navigation-pill double transitions and page jumping.
- Fixed deprecated API warnings, nullability warnings, selector warnings, and duplicate linker configuration.
- Added automatic build-version management.

- Prolly more than I can list.

v2.2.1-2
-- Fixed issue with changing store region

-- Added AppStore descriptions, screenshots and reviews

-- Added ability to download apps no longer available on AppStore/not on device

-- Fixed an issue with 2FA when logging in Settings. Remember you can always put that 2FA code in on your next sign in, directly after the password (no space.)

-- Added an option to enable logs when you have an error or weird behavior. Enabled logs, replicate the bug and send an email within the app with logs attached. 

-- Prolly more bug fixes, like STDQ and purchase settings
 


v2.1.1-1
-- Ability to buy apps you do not own (for instance if you cannot buy because the app was updated to an incompatible version before trying to purchase)

-- Page indicator to show app has more than one page

-- Ability to sign into your Apple account to parse versions faster and without the spam Download Compatible version prompts.


v2.0.1-2
-- No longer relies on my server.
-- Total app overhaul
-- Ability to search apps on the appstore. Did't really test it, so might run into some bugs. 

v1.0.3-1
-- Ability to download AppStore++ updates & open in TrollStore

v1.0.2-1
-- iPad support hopefully
-- iOS13 support
-- Back to using my reliable server.




Todos: 

1. one day not require sign in. 
