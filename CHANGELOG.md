# Changelog

All notable changes to this project will be documented in this file.

## [1.6.2] - 2025-008-004 011.035.049.160587800 America/New_York 2025-W032-001 2025-216

- version removed from README citation.

## [1.6.1] - 2025-008-004 011.030.058.059279200 America/New_York 2025-W032-001 2025-216

- version field removed from CITATION.cff. It was too much hassle [to keep up to date].

## [1.6.0] - 2025-008-002 012.010.041.314482100 America/New_York 2025-W031-006 2025-214

- I forgot to add generate_pdb_name_from_timestamp to peter_cullen_burbery_python_functions/date_time_functions/__init__.py slash peter_cullen_burbery_python_functions/__init__.py.

## [1.5.2] - 2025-008-002 009.048.016.919089700 America/New_York 2025-W031-006 2025-214

- date-released: removed from CITATION.cff. It's too much of a hassle. date-released: is too much of a hassle to keep up to date.

## [1.5.1] - 2025-008-002 008.056.016.935859000 America/New_York 2025-W031-006 2025-214

- README.md updated for PyPi.

## [1.5.0] - 2025-008-002 008.030.055.163275400 America/New_York 2025-W031-006 2025-214

## 📦 Release Notes – `date_time_stamp` v1.5.0

**Release Date:** August 2, 2025  
**Version:** 1.5.0  
**Type:** Feature & Precision Upgrade

---

### 🚀 New Features & Enhancements

- **True Nanosecond Precision Implemented**
  - Switched to `time.time_ns()` to capture the **actual system nanoseconds** since the Unix epoch.
  - Ensures **accurate sub-second precision** instead of estimated nanoseconds (previously derived from `microsecond * 1000`).

- **High-Fidelity Time Construction**
  - Time is now constructed from the **exact nanosecond timestamp**, ensuring **synchronized precision** between date and time components.

- Note: On Windows, you will only get 7 digits of precision. "055.163275400", not "055.163275412".

---

### 📚 Example Output
```text
2025-008-002 018.049.021.123456789 America/New_York 2025-W032-006 2025-214
```

**Format:**
```
YYYY-MMM-DDD HHH.MMM.SSS.NNNNNNNNN TZ_NAME YYYY-Www-ddd YYYY-DDD
```

---

### 🧼 Deprecations
- Removed simulated nanosecond logic based on `microsecond * 1000`. This was misleading and is no longer necessary.

---

## [1.4.0] - 2025-008-002 007.059.016.863518400 America/New_York 2025-W031-006 2025-214

- release for Python publish workflow.

## [1.3.0] - 2025-008-002 007.006.054.271277800 America/New_York 2025-W031-006 2025-214

- Added Zenodo information to including, but not limited to, CITATION.cff, and README.md.

## [1.2.0] - 2025-008-002 006.055.056.016237200 America/New_York 2025-W031-006 2025-214

- release for Zenodo.

## [1.1.0] - 2025-008-002 006.032.020.779609400 America/New_York 2025-W031-006 2025-214

- date_time_stamp type hints enabled.
- generate_pdb_name_from_timestamp added.

## [1.0.0] - 2025-07-30

### Changed

- validate_Windows_filename_with_reasons now accepts Union[str, Path] instead of str.
- valid_Windows_filename now accepts Union[str, Path] instead of str.

### Documentation

- Updated docstrings for validate_Windows_filename_with_reasons and valid_Windows_filename
  to reflect support for pathlib.Path input.

## [0.9.2] - 2025-07-30

### Documents

- Too specific image_functions fixed.

## [0.9.1] - 2025-07-30

### Documents

- Fixed date_time_functions/image_functions/system_management_functions to use simpler module comments.

## [0.9.0] - 2025-07-30

### Documentation

- Added module-level docstring to `image_functions.py`:
  - Summarizes image comparison functionality
  - Lists all comparison techniques used (SHA-256, ImageChops, SSIM, ImageMagick)
  - Describes function responsibilities and external tool requirements

- Added module-level docstring to `system_management_functions.py`:
  - Describes utilities provided: GitHub URL conversion, Windows filename validation, file size analysis
  - Lists external dependency: `requests`

### Improved

- Streamlined all module-level docstrings to be concise and readable
- Aligned function summaries and terminology across modules for consistency

## [0.8.0] - 2025-07-30

### Added

- Complete docstring for `date_time_stamp()` function, including:
  - Precise return format
  - Example usage
  - Explanation of all calendar components (Gregorian, ISO, ordinal)

- Module-level docstring for `date_time_functions.py`

### Improved

- Code clarity: used more explicit variable names like `local_timezone`
- Return formatting consistency using f-strings
- Enhanced maintainability with grouped logic and multiline return

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