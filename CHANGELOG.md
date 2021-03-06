# Change Log
All notable changes to this project will be documented in this file.
This project adheres to [Semantic Versioning](http://semver.org/).

## [Unreleased][unreleased]

## [1.1.0] - 2016-03-30
### Added
- Better extensibility with support for Tornado
- Support for inline images
- Support for specifying IP pool

### Fixed
- Issue where substitution data was being improperly passed to the templates preview endpoint
- Issue where Django backend was not properly base64 encoding attachments

## [1.0.5] - 2016-03-18
### Fixed
- Issue where global Django settings object was being modified, causing mixed emails

## [1.0.4] - 2016-03-10
### Added
- `SPARKPOST_OPTIONS` setting for Django for passing through additional transmission options like `track_opens`, `track_clicks`, and `transactional`
- Support for cc, bcc, reply to, and attachments for Django

### Changed
- Refactored some of the bits in the Django email backend out into a `SparkPostMessage` class which prepares parameters for calls to the `Transmissions.send` method

## [1.0.3] - 2016-03-03
### Added
- Tox for local testing
- Allow unicode recipients
- Automatically parse emails with friendly from e.g. `Friendly Name <hi@example.com>`
- Support for cc/bcc

## [1.0.2] - 2016-02-25
### Added
- Support for attachments via the `attachments` parameter in `Transmissions`

## [1.0.1] - 2016-02-25
### Fixed
- Subpackages now get included properly
- Updated examples to use plural `transmissions`

## [1.0.0] - 2015-11-06
### Added
- Django email backend
- Support for scheduled sending via the `start_time` parameter in `Transmissions`
- Support for marking messages as transactional or non-transactional via the `transactional` parameter in `Transmissions`
- Support for skipping suppression (SparkPost Elite only) via the `skip_suppression` parameter in `Transmissions`

## [1.0.0.dev2] - 2015-09-01
### Added
- Code coverage via [coveralls]
- CONTRIBUTING file for notes on how to contribute
- `Templates` class to manage templates
- `RecipientLists` class to manage recipients we want to send to
- `SuppressionLists` class to manage recipients that are suppressed

### Changed
- Renamed `Transmission` class to `Transmissions` (backwards compatible)

### Removed
- Tox file for running tests in favor of `make test` and Travis CI

### Fixed
- Engagement tracking no longer automatically enabled for all transmissions
- Documentation generation issues

## 1.0.0.dev1 - 2014-02-09
### Added
- Base SparkPost class
- `Transmission` class for sending messages
- Examples for Transmission usage
- Metrics class for getting a list of campaigns and domains
- Docs on readthedocs.org

[unreleased]: https://github.com/sparkpost/python-sparkpost/compare/v1.1.0...HEAD
[1.1.0]: https://github.com/sparkpost/python-sparkpost/compare/v1.0.5...v1.1.0
[1.0.5]: https://github.com/sparkpost/python-sparkpost/compare/v1.0.4...v1.0.5
[1.0.4]: https://github.com/sparkpost/python-sparkpost/compare/v1.0.3...v1.0.4
[1.0.3]: https://github.com/sparkpost/python-sparkpost/compare/v1.0.2...v1.0.3
[1.0.2]: https://github.com/sparkpost/python-sparkpost/compare/v1.0.1...v1.0.2
[1.0.1]: https://github.com/sparkpost/python-sparkpost/compare/v1.0.0...v1.0.1
[1.0.0]: https://github.com/sparkpost/python-sparkpost/compare/1.0.0.dev2...v1.0.0
[1.0.0.dev2]: https://github.com/sparkpost/python-sparkpost/compare/1.0.0.dev1...1.0.0.dev2
[coveralls]: https://coveralls.io/github/SparkPost/python-sparkpost
