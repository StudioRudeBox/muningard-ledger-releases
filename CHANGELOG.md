# Changelog

All notable changes to this project are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.3.1] - 2026-08-17

### Changed

- Changed the accent color used for the Accounting section.
- The "up to date" indicator on the Onderhoud settings page now appears as a badge next to the current version number, instead of as separate text below it.
- Segmented controls (like the document type selector) now switch instantly between options instead of sliding.

### Fixed

- Fixed misaligned option text in the Bron and Status filter dropdowns on the Journaal-overzicht page.

## [1.3.0] - 2026-08-17

### Added

- Full control over app updates (Settings → Onderhoud): the app still checks for new versions automatically, but now shows a notification instead of downloading and installing right away. From there you can review the release notes, choose when to download, and choose when to install — with a progress indicator while downloading. Previously, updates downloaded and installed automatically in the background.
- Expenses can now be booked and marked as paid in one action, via a new split-button control on the expense form.

### Changed

- Combined the Offertes, Verkoopfacturen, and Uitgaven settings into a single "Financieel" tab, with the sections stacked one below the other. Settings tabs are now ordered Algemeen, Financieel, Btw, MCP, Onderhoud.
- Renamed the Backup tab to "Onderhoud".
- Updated the sidebar icons for the Beheer menu and the Instellingen page.
- Moved VAT filings and fixed assets (depreciation) from their own sidebar pages into new tabs on the Accounting page.
- Shortened some Accounting tab names for a cleaner fit: "Winst- en verliesrekening" → "Winst- en verlies", "Handmatige boekingen" → "Boekingen", "Journaal-overzicht" → "Journaal".
- Recurring expenses now use the same icon as regular expenses in the sidebar and lists.
- The dimmed icon styling for pending records in list tables is now applied consistently across all sections.
- Added a divider to segmented controls for clearer visual separation between options.

## [1.2.0] - 2026-08-16

### Added

- MCP server settings (Settings → MCP): turn the MCP server on or off, and choose per section — none, read-only, or read + write — how much access an MCP client like Claude Code has to your data. Previously the server was always on if connected, with no way to control access.
- Backup export files are now compressed and include your chart of accounts, journal entries, and VAT code settings, so a restore reproduces your bookkeeping setup more completely.
- Importing a backup now asks for confirmation before overwriting your current data.

### Changed

- Expense date field is now labeled "Boekdatum" instead of "Datum uitgave".
- Refined light-mode colors, including status badges.
- Updated several sidebar icons to a filled style.
- Minor position adjustment to the notification badge in the title bar.

### Fixed

- Fixed an error when importing a compressed backup file.
- Fixed the Windows installer using the wrong file name.
- Fixed a color mismatch in light mode.
- Fixed toast notification button text using the wrong font.

## [1.1.0] - 2026-08-15

### Added

- Light mode: a new Theme setting (Settings → General) lets you choose Light, Dark, or System — System automatically follows your operating system's appearance, including live switching if you change it while the app is open. The whole app, including status badges, dashboard charts, and the window title bar, adapts to the selected theme.

### Changed

- Removing your profile photo now happens by hovering it and clicking the trash icon that appears, instead of a separate button.
- Made the global search result popover the same width as the search field.

## [1.0.1] - 2026-08-15

### Added

- Automatic update checks: the app checks for new releases on startup, downloads them in the background, and prompts to restart once ready.

## [1.0.0] - 2026-08-15

First production release.

### Added

- Relations (clients/suppliers) management.
- Invoices and quotes, with line items and status tracking.
- Expenses and recurring expenses.
- Depreciation / fixed-asset register.
- Client expirations register.
- Quarterly Dutch VAT report and VAT filings.
- Dashboard with checklist overview.
- Manual `.db` file backup.
- Read-only MCP server (`ping`/`health` plus `list_X`/`get_X` tools per entity) for use with Claude Code.
