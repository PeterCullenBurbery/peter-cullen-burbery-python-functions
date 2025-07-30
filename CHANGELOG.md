# Changelog

All notable changes to this project will be documented in this file.

## [0.6.1] - 2025-07-29

### Fixed

- Exposed `valid_Windows_filename()` at the top-level package interface via `__init__.py`
  - You can now import it directly from `peter_cullen_burbery_python_functions.system_management_functions`

## [0.6.0] - 2025-07-29

### Added

- Added `valid_Windows_filename()` to `system_management_functions` subpackage  
  - Returns a boolean indicating whether a Windows filename is valid  
  - Simple wrapper around `validate_Windows_filename_with_reasons()`  

### Improved

- `validate_Windows_filename_with_reasons()` now loads its validation rules from a GitHub-hosted JSON file using a hardcoded blob URL and `requests` with retry logic

## [0.5.0] - 2025-07-28

### Added

- Added `validate_Windows_filename_with_reasons()` to `system_management_functions` subpackage  
  - Validates Windows filenames using a GitHub-hosted JSON schema  
  - Returns structured reasons for invalid characters, reserved names, and trailing space/dot

## [0.4.0] - 2025-07-28

### Added

- Added `convert_blob_to_raw_github_url()` to `system_management_functions` subpackage  
  - Transforms GitHub blob URLs to raw URLs

## [0.3.1] - 2025-07-25

### Documentation

- Updated `README.md`.

## [0.3.0] - 2025-07-25

### Added

- Introduced `image_functions` subpackage  
- Added `compare_images()` function with:  
  - SHA-256 hash comparison  
  - Pixel difference via Pillow (ImageChops)  
  - SSIM metric via scikit-image  
  - ImageMagick AE metric with visual diff output

## [0.2.0] - 2025-07-25

### Changed

- Reorganized `date_time_stamp` into `date_time_functions` subpackage

## [0.1.0] - 2025-07-22

- Initial release with `date_time_stamp()` function