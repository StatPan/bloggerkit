# Change Log

All notable changes to this project will be documented in this file.

## [0.7.0] - 2025-06-06

### Added
- **Environment Variable Support**: Now supports `GOOGLE_CLIENT_ID` and `GOOGLE_CLIENT_SECRET` environment variables for authentication
- **Auto-generated Credentials**: Automatically creates `credentials.json` when using environment variables
- **Enhanced Post Creation**: Added `labels` and `is_draft` parameters to `create_post()` method
- **Enhanced Post Update**: Added `labels` parameter to `update_post()` method
- **Improved Logging**: Added informative messages throughout the authentication and posting process
- **Better Error Messages**: More helpful error messages with setup instructions

### Changed
- **Flexible Authentication**: `BloggerClient` constructor now accepts optional `client_id` and `client_secret` parameters
- **Authentication Priority**: Environment variables > Direct parameters > `client_secrets_file`
- **Enhanced Token Management**: Improved token refresh and error handling
- **Better User Experience**: Clear status messages during authentication and posting

### Backward Compatibility
- **Fully Compatible**: All existing code using `client_secrets_file` continues to work unchanged
- **Gradual Migration**: Users can choose to migrate to environment variables at their own pace

## [0.6.0] - 2025-03-23

### Added
- OAuth 2.0 authentication support.
- `client_secrets.json` file is now required for authentication.

### Changed
- `BloggerClient` constructor now takes `blog_id` and `client_secrets_file` as arguments.

### Removed
- `api_key` argument from `BloggerClient` constructor.