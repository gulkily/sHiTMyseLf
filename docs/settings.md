# Pollyanna Settings Documentation

This document provides a comprehensive list of all settings in Pollyanna, including their purpose, values, and source file references.

This document was generated by claude-3.5-sonnet, and have not been proofread closely yet.

## Table of Contents
1. [GPG Settings](#gpg-settings)
2. [Image Processing Settings](#image-processing-settings)
3. [Server Authentication Settings](#server-authentication-settings)
4. [PHP Settings](#php-settings)
5. [Security Settings](#security-settings)
6. [Theme Settings](#theme-settings)
7. [Upload Settings](#upload-settings)
8. [Development Settings](#development-settings)
9. [Performance Settings](#performance-settings)
10. [URL Management Settings](#url-management-settings)
11. [Cookie Management Settings](#cookie-management-settings)
12. [Response Handling Settings](#response-handling-settings)

## GPG Settings

### `admin/gpg/enable`
- **Purpose**: Master switch for GPG integration
- **Values**: 0/1
- **Source Files**:
  - `default/template/perl/file.pl`: GPG file operations
  - `default/template/perl/index_text_file.pl`: Text file indexing and signing

### `admin/gpg/use_gpg2`
- **Purpose**: Uses GPG2 instead of GPG1
- **Values**: 0/1
- **Source Files**:
  - `default/template/perl/gpg.pl`: GPG version selection
  - `default/template/perl/utils.pl`: GPG utility functions

### `admin/gpg/sign_operator_response`
- **Purpose**: Signs operator responses with GPG
- **Values**: 0/1
- **Source Files**:
  - `default/template/perl/index_text_file.pl`: Operator response signing
  - `default/template/perl/server_response.pl`: Response handling

## Image Processing Settings

### `admin/image/enable`
- **Purpose**: Master switch for image features
- **Values**: 0/1
- **Source Files**:
  - `default/template/perl/index_file.pl`: File indexing
  - `default/template/perl/index_zip_file.pl`: ZIP file handling
  - `default/template/perl/dialog/stats_table.pl`: Statistics display
  - `default/template/perl/index.pl`: Main indexing
  - `default/theme/ilyag/template/perl/page/welcome.pl`: Welcome page

### `admin/image/allow_files`
- **Purpose**: Controls file upload types
- **Values**: Comma-separated extensions (e.g., "jpg,png,gif")
- **Source Files**:
  - `default/template/perl/index_file.pl`: File type validation
  - `default/template/perl/index_zip_file.pl`: ZIP content validation
  - `default/template/perl/dialog/upload.pl`: Upload handling
  - `default/template/perl/utils.pl`: Utility functions

### `admin/image/thumbnail_extension`
- **Purpose**: Sets thumbnail file extension
- **Values**: String (e.g., "jpg", "png")
- **Source Files**:
  - `default/template/perl/render_field.pl`: Field rendering
  - `default/template/perl/image_thumbnail.pl`: Thumbnail generation
  - `default/template/perl/image_container.pl`: Image container handling
  - `default/template/perl/video_thumbnail.pl`: Video thumbnail handling

## PHP Settings

### `admin/php/enable`
- **Purpose**: Master switch for PHP features
- **Values**: 0/1
- **Source Files**:
  - `default/template/perl/dialog/write.pl`: Write dialog
  - `default/template/perl/widget/menu.pl`: Menu generation
  - `default/theme/flyerian/template/perl/page/welcome.pl`: Welcome page

### `admin/php/debug`
- **Purpose**: Enables PHP debug output
- **Values**: 0/1
- **Source Files**:
  - `default/template/php/handle_not_found.php`: Debug output
  - `default/template/perl/utils.pl`: Debug utilities

### `admin/php/light_mode_default`
- **Purpose**: Sets default light mode
- **Values**: 0/1
- **Source Files**:
  - `default/template/perl/page_header.pl`: Header generation
  - `default/template/perl/theme_select.pl`: Theme selection

### `admin/php/light_mode_always_on`
- **Purpose**: Forces light mode
- **Values**: 0/1
- **Source Files**:
  - `default/template/perl/page_header.pl`: Header generation
  - `default/template/perl/theme_select.pl`: Theme selection

## Security Settings

### `admin/server_vouch/enable`
- **Purpose**: Enables server vouching
- **Values**: 0/1
- **Source Files**:
  - `default/template/perl/utils.pl`: Server authentication
  - `default/template/perl/server_response.pl`: Response handling

### `admin/voting/require_fingerprint`
- **Purpose**: Requires fingerprint for votes
- **Values**: 0/1
- **Source Files**:
  - `default/template/perl/vote_check.pl`: Vote validation
  - `default/template/perl/vote_process.pl`: Vote processing

## Upload Settings

### `admin/php/upload/strip_exif`
- **Purpose**: Removes EXIF data from uploads
- **Values**: 0/1
- **Source Files**:
  - `default/template/perl/image_process.pl`: Image processing
  - `default/template/perl/upload_handle.pl`: Upload handling

### `admin/php/route_upload_require_cookie`
- **Purpose**: Requires cookie for uploads
- **Values**: 0/1
- **Source Files**:
  - `default/template/php/upload.php`: Upload endpoint
  - `default/template/perl/upload_check.pl`: Upload validation

## Development Settings

### `admin/debug_use_milliseconds`
- **Purpose**: Uses millisecond precision in logs
- **Values**: 0/1
- **Source Files**:
  - `default/template/perl/utils.pl`: Timing functions
  - `default/template/perl/logging.pl`: Log formatting

### `admin/git_cron_pull`
- **Purpose**: Enables automatic git pulls
- **Values**: 0/1
- **Source Files**:
  - `default/template/perl/git_pull.pl`: Git operations
  - `default/template/perl/cron.pl`: Cron job handling

## Performance Settings

### `admin/php/debug_do_not_use_cache`
- **Purpose**: Disables caching for debugging
- **Values**: 0/1
- **Source Files**:
  - `default/template/perl/cache.pl`: Cache control
  - `default/template/php/page.php`: Page generation

### `admin/php/regrow_keep_fresh_interval`
- **Purpose**: Sets page refresh interval
- **Values**: Numeric (seconds)
- **Source Files**:
  - `default/template/perl/page_utils.pl`: Page regeneration
  - `default/template/php/handle_not_found.php`: 404 handling

## URL Management Settings

### `admin/php/url_alias_friendly`
- **Purpose**: Enables friendly URLs
- **Values**: 0/1
- **Source Files**:
  - `default/template/php/route.php`: URL routing
  - `default/template/perl/url_alias.pl`: Alias handling

### `admin/php/alias_lookup`
- **Purpose**: Enables URL alias system
- **Values**: 0/1
- **Source Files**:
  - `default/template/perl/url_alias.pl`: Alias resolution
  - `default/template/php/route.php`: URL routing

## Cookie Management Settings

### `admin/php/route_cookie_enable`
- **Purpose**: Enables cookie functionality
- **Values**: 0/1
- **Source Files**:
  - `default/template/php/handle_not_found.php`: 404 handling
  - `default/template/perl/page_footer.pl`: Page footer generation

### `admin/php/cookie_inbox`
- **Purpose**: Enables inbox cookie tracking
- **Values**: 0/1
- **Source Files**:
  - `default/template/perl/inbox.pl`: Inbox handling
  - `default/template/php/cookie.php`: Cookie management

## Response Handling Settings

### `admin/php/server_response_display_to_client`
- **Purpose**: Shows server responses
- **Values**: 0/1
- **Source Files**:
  - `default/template/perl/server_response.pl`: Response formatting
  - `default/template/php/response.php`: Response handling

### `admin/php/server_response_attach_to_anchor`
- **Purpose**: Attaches responses to anchors
- **Values**: 0/1
- **Source Files**:
  - `default/template/perl/page_render.pl`: Page rendering
  - `default/template/perl/server_response.pl`: Response attachment

## Setting Dependencies

Some settings have dependencies on others:

1. Image Processing Chain:
   - `admin/image/enable` must be 1 for other image settings to work
   - `admin/php/upload/strip_exif` requires `admin/image/enable`

2. Cookie Security Chain:
   - `admin/php/route_cookie_enable` must be 1 for cookie-dependent features
   - `admin/php/cookie_inbox` requires `admin/php/route_cookie_enable`

3. GPG Chain:
   - `admin/gpg/enable` must be 1 for other GPG settings
   - `admin/gpg/sign_operator_response` requires `admin/gpg/enable`

## Configuration Examples

### Secure Upload Configuration
```bash
hike set admin/php/upload/strip_exif 1
hike set admin/php/route_upload_require_cookie 1
hike set admin/image/allow_files "jpg,png,gif"
```

### Development Environment
```bash
hike set admin/debug_use_milliseconds 1
hike set admin/php/debug_do_not_use_cache 1
hike set admin/php/server_response_display_to_client 1
```

### Production Security
```bash
hike set admin/gpg/enable 1
hike set admin/gpg/sign_operator_response 1
hike set admin/server_vouch/enable 1
```

## Troubleshooting

1. **Image Upload Issues**
   - Verify `admin/image/enable`
   - Check allowed file types
   - Verify EXIF stripping if enabled

2. **Authentication Problems**
   - Check server vouch settings
   - Verify cookie configuration
   - Check GPG settings if using signed responses

3. **Performance Issues**
   - Review cache settings
   - Check page regeneration intervals
   - Verify debug settings in production