# Changelog

All notable changes to this project are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

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
