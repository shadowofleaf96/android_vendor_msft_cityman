# Vendor Tree for Microsoft Lumia 950 XL (Cityman)

This repository contains the proprietary vendor blobs extracted from the stock Windows Mobile firmware and subsequent Android ports for the Microsoft Lumia 950 XL (RM-1085).

## Changelog

### [Unreleased]

#### Added / Modified
- **Camera Blobs**: Replaced the incorrect IMX377 camera blobs with the correct IMX230 camera blobs (e.g., `libmmcamera_imx230.so`, `libchromatix_mot_imx230_*.so`, `libSonyIMX230PdafLibrary.so`).
- **RIL / Baseband**: Included a custom-patched `libqmi_cci.so` to facilitate the wrapper interception.
- **Sensors / PM**: Included a patched `libvss_nv_core.so` to bypass restrictive power management calls that caused infinite boot loops.
- **Cleanup**: Removed incompatible Nexus 5X (Angler) `libsensor1` and `sensors.ssc.so` binaries to allow the native HAL to load properly.
