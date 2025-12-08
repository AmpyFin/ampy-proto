# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.1.1] - 2025-02-08

### Added
- Enhanced documentation with comprehensive design principles and schema reference
- Detailed development guide with prerequisites and build instructions
- Complete examples for Python, Go, and C++ implementations

### Changed
- Merged comprehensive documentation from README_ampy-proto.md into main README.md
- Updated all version references to 2.1.1 across documentation and package files
- Improved repository structure and documentation organization

### Fixed
- Verified and confirmed resolution of protobuf descriptor corruption issues from v2.0.6
- All language implementations (Python, Go, C++) tested and verified working correctly

## [2.0.9] - 2024-12-19

### Fixed
- Fixed Go module structure for proper pkg.go.dev indexing by moving convenience package to `pkg/ampy/`
- Resolved package conflicts that caused pkg.go.dev to display module as "smoke" instead of "ampy-proto"
- Updated all version references to 2.0.9 across documentation and package files

### Changed
- Moved convenience package from root `ampy.go` to `pkg/ampy/ampy.go` for better module organization
- Updated import path for convenience package: `github.com/AmpyFin/ampy-proto/v2/pkg/ampy`
- Updated README with correct installation commands and import examples

## [2.0.8] - 2024-12-19

### Fixed
- Fixed protobuf generation compatibility issues with protoc-gen-go v1.36.8
- Resolved slice bounds errors that caused runtime panics
- Updated import paths to use correct v2 module structure
- Synchronized protobuf versions across all language bindings

### Changed
- Updated Go examples to use correct import paths and types
- Improved smoke tests for all supported languages
- Enhanced build process reliability

## [2.0.7] - 2024-12-19

### Fixed
- Initial fix for protobuf descriptor corruption
- Updated to protoc-gen-go v1.35.2 for compatibility

## [2.0.6] - 2024-12-19

### Added
- Initial release of ampy-proto v2
- Support for Go, Python, and C++ code generation
- Comprehensive schema definitions for financial data
- High-precision decimal types for price data
- Time discipline with event/ingest time separation
- Security identification with MIC codes
- Metadata support for data lineage

### Security
- All timestamps are UTC with clear semantics
- Proper security identification beyond ticker symbols
- Scaled decimal types prevent floating-point precision errors
