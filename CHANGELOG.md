# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.1.0] - 2026-04-21

### Added
- Notification support for `edited` events for both discussions and comments.
- New `events` input to filter which actions should trigger notifications (default: `created`).
- Message body preview: now the first 255 characters of the discussion or comment are included in the notification.
- HTML escaping for message titles and bodies to prevent notification delivery failures.
- Comprehensive `README.md` in both English and Russian.
- This `CHANGELOG.md` file.

### Changed
- Improved message formatting in Telegram.

## [1.0.0] - 2026-04-20

### Added
- Initial release.
- Basic notifications for new discussions and comments.
- Support for RU/EN languages.
- User mapping support.
- Support for Telegram Thread ID.
