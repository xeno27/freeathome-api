# Changelog

### Unreleased

* **Bug Fix:** Fixes a startup crash (`TypeError: Cannot read properties of undefined (reading 'name')` in `XmlParser.parseDeviceData`) that occurred when a channel references a floor uid that is not present in the floorplan data — e.g. the special `FD` "default floor" (which is skipped while building `floorData`) or a deleted floor. Floor/room are now resolved defensively and fall back to an empty string instead of crashing the whole API.

### 1.1.3 (2023-01-30)

* **Bug Fix:** Fixes a possible crash when a device is assigned to a floor but placed outside any room (#45).
* **Enhancement:** Update documentation with some technical details regarding *functionIds*. (#47)

### 1.1.2 (2022-10-09)
* **Enhancement:** Add support for System Access Point firmwares >= 3.0.1
* **Enhancement:** Update dependencies

### 1.1.1 (2020-08-11)
* **Enhancement:** Report error responses
* **Enhancement:** Broadcast subscriber status
* **Enhancement:** Connection handling improved (#24)
* **Bug Fix:** Fixed symmetric nonce sequence
* **Bug Fix:** Fixed update message filtering to prevent crash (#18)

## 1.1.0 (2019-12-28)

* **Enhancement:** Improved Error Handling (#12)
* **Enhancement:** Allow API to be used as a library (#8)
* **Enhancement:** Added channel/datapoint parameter to *info* API endpoint (#3)
* **Enhancement:** Expose Room/Floor names/id and display name (#4)
* **Bug Fix:** Fixed Firmware Version Check (#13)
* **Bug Fix:** Correctly process accessories which are not ready on discovery
* **Bug Fix:** Fixed Docker Image (#17)

### 1.0.1 (2019-09-30)
* Added support for environment variables to configure the API
* Added docker image

## 1.0.0 (2019-09-29)

Initial Release
