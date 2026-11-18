# TorkeToolkit — Update History (Changelog)

## v3.2.0 (Consolidated Release)

### Official Driver Center & Simultaneous Downloads
- **Driver Center Without Windows Update (`DriverCenterWindow`):** scans your CPU, all GPUs, and core hardware drivers (`Win32_PnPSignedDriver` + `Win32_Processor` + `Win32_VideoController`), queries WHQL driver updates directly over HTTP from **Microsoft Update Catalog** and the **NVIDIA Official API**, supports multi-select queuing / **Select All (Updates)**, installs `.cab` packages via `pnputil`, and enforces an **INPUT/USB** safety shield.
- **Simultaneous Downloads (`1x`–`5x`) & Real-Time Percentages:** the Software Installer now includes a concurrency selector (`1x` to `5x`) with aggregated global progress (`0%`–`100%`) and live percentages across Winget, Chocolatey, direct downloads, Driver Center, and Self-Updater.

## v3.1.0 (Accumulated Features)

### Battery Guard, Smart Charging & Preventive Self-Diagnostics
- **Battery Health, Cycle Count & Smart Charge (`TORKE BATTERY GUARD`):** native telemetry via `IOCTL_BATTERY_QUERY_INFORMATION` + WMI (Health %, Wear %, Charge Cycles, Full vs Design mWh, Voltage, and Wattage). Includes **Fixed Cap (60–85%)**, **Scheduled Departure**, and **Adaptive Learning** (`PowerModeChanged`) with native adapters for **ASUS** (`ATKACPI` + `AsusAtkWmi_WMNB`), **Dell** (`DCIM_BIOSService` WMI + `cctk.exe`), **HP** (`root\HP\InstrumentedBIOS` Battery Health Manager), and **Lenovo** (`EnergyDrv` + `PWRMGRV`), plus universal **HTTP Smart Plug** and tray alerts. Available from **Tier 1**.
- **12-Point Full Failure Self-Diagnostic:** preventive checker for critical `C:` free space, S.M.A.R.T. health, CPU/GPU/Disk thermal warnings, PnP driver errors (`ConfigManagerErrorCode`), battery wear, RAM/Pagefile pressure, essential services, pending reboot, recent BSOD Minidumps, network/DNS health, Windows Firewall, and VC++ runtimes.

### Real-Time Telemetry & Hardware Audit
- **Native `LibreHardwareMonitorLib` Engine:** live CPU, GPU & Disk temperatures (`°C`), core clocks (`MHz`), combined PC power draw (`CPU + RAM RAPL + GPU + Base` / `PSU` / `Battery`), network throughput (`↓/↑ KB/s`), and fan speeds (`RPM`).
- **Torke Lab Monitor:** 4 color-coded KPI cards, live oscilloscope graph (`CPU / RAM / GPU` with shaded area), 1-click **Trim RAM**, **Battery 80%**, and **Hardware Audit**. Available in **Tier 1**.
- **9-Tab Hardware & Sensors Audit:** `Overview` (with Torke Health Matrix), `Processor` (core topology, caches, AVX/SSE/AES), `Graphics` (driver age & VRAM), `Memory` (DIMM modules & channels), `Motherboard` (BIOS, VBS, HVCI, TPM, Secure Boot), `Storage` (drives, volumes & TRIM), `Network`, `Windows`, and `Sensors (1s)` + privacy-safe JSON export.

### Gaming Pro, MiniOS X & Personalization
- **+1,000 Games & Emulators in Game Booster:** expanded `GameBoosterService` detection covering PC games and major emulators (PCSX2, RPCS3, Dolphin, Cemu, Ryujinx, Yuzu/Suyu, DuckStation, PPSSPP, RetroArch, Xenia, Vita3K, MAME, BlueStacks, LDPlayer, and 1,000+ titles).
- **Portable & Customizable MiniOS X:** 16 independent modules (`MiniOsConfigWindow`), 3 quick presets, automatic `minios-profile.json` persistence, and USB JSON Export/Import.
- **High-Contrast Light Theme:** tuned surfaces, borders, sidebar contrast, live log console, adaptive accents (`TorkeCyan`/`TorkeBlue`), and System tab polish.

### Installer, Deep Uninstaller & Licensing
- **Deep Uninstaller Pro (Revo-style):** leftover AppData/Registry/shortcut scanner, blocking process killer, ACL repair, pending-delete on reboot (`MoveFileEx`), forced removal, batch uninstall, Winget quick upgrade, and async local **real app icons** (0 KB bloat).
- **Resilient +140-App Installer:** configurable channels (**Winget / Chocolatey / Direct**) with automatic failure memory, `.part` atomic download + SHA-256 / magic-byte validation, and custom Downloads directory.
- **Unified Tier 3 USB Licensing & Private KeyGen:** a single Tier 3 license key activates Portable USB Mode automatically without needing dual keys.

## Earlier Releases (v3.0.x – v3.1.0 base)
- Full **English / Spanish** multi-language UI architecture with automated XAML validation.
- Deep Shader/Cache Cleaner, Startup Manager, UWP Bloatware Remover, Document Converter/Merger, Tray Eco Mode, and Technician Workshop with PDF Before/After Benchmark export.

