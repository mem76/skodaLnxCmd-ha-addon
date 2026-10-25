# Changelog

## 0.3.3 - 2026-10-22
### Changed
- Force HA to rebuild container if OS-updates exist. (increased security)

## 0.3.2 - 2026-10-22
### Changed
- None (force rebuild to force important security update)

## 0.3.1 - 2026-10-18
### Changed
- Abort and return error on non-valid data.

## 0.3.0 - 2026-10-18
- Add guard config code for "0km" odometer from MyŠkoda API.
- Fix typo in "stop AC" button.

## 0.2.2 - 2026-10-18
### Added
- New entities: 
  - vehicle image URI
  - is home
- Option for disabling GPS/locations data
- Add AC off

### Changed
- Handle negative charge rates (due to AC or battery heater)
- Add guard code for "0km" odometer from MyŠkoda API.

## 0.2.1 - 2026-10-15
### Changed
- Updated to API v1.1.0
- Abort cache purge if rate-limit-left is low
- Small fix to the yaml-config
 
## 0.2.0 - 2026-10-13
### Changed
- Stabilize the app

## 0.1.1 - 2026-10-11
### Added
- Add current charging profile support.

### Changed
- Improved YAML sample file

## 0.1.0 - 2026-10-11
### Added
- Initial Alpha release of the Home Assistant wrapper structure.
