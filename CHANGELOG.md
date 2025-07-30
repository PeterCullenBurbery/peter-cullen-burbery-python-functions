# Changelog

All notable changes to this project will be documented in this file.

## [0.7.7] - 2025-07-30

### Documentation

- Added `Documentation` link to PyPI sidebar via `[project.urls]` in `pyproject.toml`
  - Now links to: https://peter-cullen-burbery-python-functions.readthedocs.io

- Verified sidebar links on PyPI:
  - Homepage → GitHub repo
  - Documentation → Read the Docs
  - Source → GitHub repo

## [0.7.6] - 2025-07-30

### Documentation

- Split Sphinx documentation into dedicated sections:
  - `date_time_functions`
  - `image_functions`
  - `system_management_functions`

- Updated `index.rst` to organize documentation by module

- Created individual `.rst` files for each module, using `.. automodule::` for clear and structured API references

- Improved sidebar and navigation structure on Read the Docs

## [0.7.5] - 2025-07-30

### Fixed

- Switched to using `build.jobs` in `.readthedocs.yml` for more structured control over build steps
  - Split install and build phases explicitly
  - Used `sphinx-build` to generate HTML into `$READTHEDOCS_OUTPUT/html`
- Kept `build.tools` field with `python: "3.13"` for clarity and reproducibility
- Retained `sphinx.configuration` key pointing to `docs/source/conf.py`

## [0.7.4] - 2025-07-30

### Fixed

- Updated `.readthedocs.yml` to include required `build.tools` field
  - Explicitly set Python version to `"3.13"` for compatibility with Read the Docs V2 config
  - "ubuntu-24.04" was valid.

## [0.7.3] - 2025-07-30

### Fixed

- Corrected `.readthedocs.yml` config to use a valid `build.os` key ubuntu-22.04. "ubuntu-24.04" was not valid.

## [0.7.2] - 2025-07-30

### Fixed

- Corrected `.readthedocs.yml` config to use a valid `build.os` key ubuntu-24.04. "ubuntu-lts-latest" was not valid.

## [0.7.1] - 2025-07-30

### Fixed

- Corrected `.readthedocs.yml` config to use a valid `build.os` key:

## [0.7.0] - 2025-07-30

### Documentation

- Integrated with **Read the Docs** for automatic documentation hosting
- Added `.readthedocs.yml` configuration file
- Connected repository using **GitHub OAuth**
- Configured **Sphinx** with the `sphinx_rtd_theme`
- Publicly hosted API reference and source documentation on Read the Docs

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