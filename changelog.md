# Change Log

All notable changes to this project will be documented in this file.

## [0.6.0] - 2025-03-23

### Added
- OAuth 2.0 authentication support.
- `client_secrets.json` file is now required for authentication.

### Changed
- `BloggerClient` constructor now takes `blog_id` and `client_secrets_file` as arguments.

### Removed
- `api_key` argument from `BloggerClient` constructor.