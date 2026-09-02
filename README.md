# AppStorePlus-TrollStore
AppStore++ tweak for TrollStore

Allows you to downgrade installed apps.

How to install: 
1. Install TrollStore on your device: https://github.com/opa334/TrollStore
2. Download AppStore++ [here](https://github.com/CokePokes/AppStorePlus-TrollStore/releases/download/v2.3.6-1/AppStorePlus-v2.3.6-1.tipa) from your mobile safari.
3. Open Files app and "Open in" Trollstore. & Done.

Enjoy. 

Changes: 

# AppStore++ — What’s New in v2.3.6-1

## Version browsing and downloads

- Added release-note information buttons beside available app versions.
- Added a clean release-notes viewer with version and release-date information.
- Expanded release-note coverage across older App Store and iTunes Store histories, including versions no longer shown in Apple’s current version history.
- Added automatic recovery of missing version dates without requiring users to clear and download their entire version cache again.
- Added favorite versions, displayed in a dedicated section above the complete version list.
- Redesigned version and IPA download progress with an App Store-style card, app icon, pie progress, cancellation, and background controls.
- Added an animated transition from the progress card into the download pill.
- When downloads are already visible, newly queued app icons now fly into the expanded pill or collapsed download indicator.
- IPA downloads now show their own progress card, including when other downloads are already running.
- The download pill is now created only when needed and is fully removed after the queue finishes.
- Improved multi-app and round-robin downloading so queued apps continue making progress without restarting or losing completed work.
- Fixed cancellation, pause/resume, progress totals, cache persistence, and progress being displayed for the wrong queued app.
- Fixed completed and fully cached version lookups incorrectly creating an empty download pill.

## Apple Account improvements

- Reworked optional AppStore++ Apple Account sign-in for newer versions of iOS.
- Signed-in AppStore++ accounts can now load available versions using the faster account-based path.
- AppStore++ automatically falls back to the device’s App Store account when a separate AppStore++ account is unavailable or disabled.
- Improved account status presentation in Settings and made the device account clearly read-only.
- Removed obsolete sign-in warnings and diagnostic options while retaining useful error reporting.

## Installed apps and backups

- Added favorites for installed apps, available from the app management menu and displayed in a dedicated Favorites section.
- Added notes for saved app-data backups so backups can be labeled with details such as the account or configuration they contain.
- Added a **Backups** button to the IPA Library for quick access to backups from every app.
- Added a choice to restore app data with or without saved Keychain data when a backup contains Keychain items.
- Improved Keychain restoration compatibility and reporting.
- Installed apps now refresh automatically after an IPA finishes installing.
- Added installation progress to the AppStore++ progress interface.
- Delayed installation completion notifications until installation and any requested data restoration have actually finished.
- Alphabetically sorted the IPA Library and all-app backups browser, while keeping individual files and backups ordered newest first.

## App Store and library interface

- Added search to the Updates tab.
- Filtered empty App Store review cards from app descriptions.
- Refined Manage and download controls to better match the App Store’s button styling.
- Added a new animated AppStore++ launch experience.
- Improved table-cell animations while preserving fast scrolling, search-bar interaction, and normal touch handling.
- Improved progress-card sizing, dismissal animations, download-pill spacing, and collapsed download presentation.

## Fixes and reliability

- Fixed IPA downloads using the wrong app artwork in the download manager and IPA Library.
- Fixed saved IPA sharing crashes and improved handling when a saved file is missing.
- Fixed downloads disappearing, immediately cancelling, or failing to start when multiple apps were queued.
- Fixed progress counters resetting or reducing their total when round-robin downloading resumed.
- Fixed finished installation alerts occasionally failing to appear or reporting an unknown version.
- Fixed app installation monitoring getting stuck after the requested version had successfully installed.
- Improved compatibility with TrollStore Lite and jailbreak-based installations.
- Added safe background-idle termination after five minutes when no downloads, lookups, or installations are active.
- Improved network recovery so interrupted update checks retry when connectivity returns.

---

Thank you to everyone who submitted logs, tested builds, and reported issues.



# AppStore++ — What’s New in v2.3.1-1

## IPA installation

- Added pie progress for ipa installation.
- Fixed an issue restoring keychain data for backed up apps. (May need to redo your backups for compatibility.)

## Compatibility and reliability

- App is now killed after 5 minutes of inactivity.
- Installed app list is now refreshed after installing an ipa.
- AppStore++ version update fixes.

---

Thanks!

# AppStore++ — What’s New in v2.3.0-1

## AppStore updates

- Added a dedicated **Updates** tab for installed App Store apps.
- Added an update-count badge that is populated when AppStore++ launches.
- Updates are sorted by release date and display the release notes, date, version, download size, and app icon provided by Apple.
- Every update includes an expandable App Store-style **more** button.
- Added **Update All**, with the ability to stop pending updates by pressing it again.
- Added live waiting, download-progress, installation, and **OPEN** states to update cells.
- Tapping an update opens the app’s full product-details page.
- Holding an Update button opens the AppStore++ management menu for that app.
- Fixed long app names shrinking or displacing Update buttons.
- Fixed update-count, release-note, and More-button layout issues.

## IPA installation

- Added native appstored installation for account-authorized IPAs.
- AppStore++ now prefers appstored so compatible installations retain their App Store identity.
- Automatically falls back to MobileInstallation when appstored cannot accept an IPA.
- Restored installation and IPA-download completion notifications.
- Fixed saved IPA sharing crashes caused by missing files or invalid iPad popover anchors.

## Compatibility and reliability

- Fixed Manual Install freezing or crashing after pressing **Proceed** on iOS 14.
- Removed the obsolete Manual Install web page and now proceeds directly from Bundle-ID resolution to the external-version prompt.
- Added a clear error when Manual Install cannot resolve a Bundle ID.
- Fixed crashes involving text fields when iOS Bold Text is enabled.
- Improved AppStore++ update checking so a failed check is retried after network connectivity returns.
- Expanded Simplified Chinese coverage for Updates and newer error messages.

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
