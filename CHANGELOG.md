# Changelog

All notable changes to this project will be documented in this file.

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