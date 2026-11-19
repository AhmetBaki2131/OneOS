# OneOS — YAAP Android 17 Fork for Samsung Galaxy A05 (SM-A055F)

## Upstream Attribution
- **Upstream repository:** [fahadalijaved/OneOS](https://github.com/fahadalijaved/OneOS) (base commit `ac5abc5782c832a8fcace65f66315bc4a92cc940`, OneOS `0.5.19`)
- **Original concept / credits:** [WeWaffles/OneLineage](https://github.com/WeWaffles/OneLineage), OneUIProject SESL & One UI Design (see upstream `LICENSE` and `CREDITS.md`)
- **Companion scripts & patcher repo:** [AhmetBaki2131/OneOS-YAAP](https://github.com/AhmetBaki2131/OneOS-YAAP)

## Changes in branch `yaap-a05`
- Normalized `MT6769V/CZ` -> `MT6768` (Helio G85) and added Galaxy A05 (`SM-A055`, `a05m`) profile (`Soc.kt`, `Profiles.kt`, `ApkSeries.kt`, `oneos_root.sh`).
- Added YAAP custom AOSP Android 17 host opt-in (`CustomRom.kt`, `Gates.kt`, `StageCheck.kt`).
- Accepted YAAP 55-method `IInstalld` (`1f1b94c0353fb2e69862a0f0411d70576a2bc8609e10c6788b425e0bdc41b874`) and added runtime `YaapInstalldDexPatcher.kt` remapping `OneOSInstalldProxy` fsverity slots `53->52` & `54->53` in `services_patched.jar` (`InstalldTable.kt`, `AppAssets.kt`, `PrepareJob.kt`).
- Added `imsd` / `ro.product.locale` guards (`oneos_switch.sh`) and HIDL `composer@2.x` fallback (`guest_start.sh`).
