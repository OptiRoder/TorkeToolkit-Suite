# TorkeToolkit — Update History (Changelog)

## v3.3.0 (Torke HUD, Extreme Battery Saver, Sustained CPU Boost, Win11 RAM Reducer & Dark Tray)

### Gaming Pro, Torke HUD & Sustained CPU Boost
- **Torke HUD — Real-Time ETW In-Game Telemetry Overlay (`TelemetryOverlayWindow` / `EtwFpsMonitorService`):** ultra-lightweight (`<0.3%` CPU) floating overlay displaying **real FPS, Frametime, and 1% Low via Windows ETW** (`Ctrl+Shift+O`), zero DLL injection (0% anti-cheat risk), auto-show on game launch, and compact horizontal or vertical modes.
- **Safe Sustained CPU Boost (`SetSustainedCpuBoost`):** without modifying voltages or BCLK, sets **0% AC EPP (`PERFEPP`)** for instant Intel Speed Shift / AMD CPPC clock ramp, enables **Aggressive AC Turbo Boost**, keeps **100% AC cores unparked**, and disables **Windows Power Throttling**. Applied automatically in `OptimizeGaming()` and toggleable in **Gaming Pro**.
- **Stronger Smart RAM Clean & Game Booster:** upgraded `SmartGamingPreset` (`SystemFileCache` + `ModifiedPageList` + `10 MB` background trim threshold) and added **Aggressive Boost Mode** with deep entry purge when a game launches plus stutter-free ongoing maintenance.
- **Modular & Reversible Windows 11 RAM Reducer:** 7 independent switches in **Gaming Pro** to disable/revert Copilot/Recall/Widgets/Bing WebView2, UWP background apps, Edge/Chrome Startup Boost, `SysMain`, `WSearch`, Telemetry (`DiagTrack`), and Mica/Acrylic Transparency.
- **+26 Recent & Viral Games Added to Auto-Detection:** covers Extraction, Action RPG, Simulation, and Viral Co-op hits (*Monster Hunter Wilds*, *Split Fiction*, *R.E.P.O.*, *Schedule I*, *Clair Obscur: Expedition 33*, *Kingdom Come: Deliverance II*, *Deadlock*, *Marvel Rivals*, *Delta Force*, *FragPunk*, *Path of Exile 2*, *inZOI*, and more).

### Battery Saver, Hardware Telemetry, Tray Menu & Splash Polish
- **Extreme Battery Saver Mode (`ExtremeBatterySaverService`) + Battery Report Viewer (`BatteryReportWindow`):** 1-click reversible battery profile (CPU Turbo OFF + 70% cap + high-efficiency EPP, display brightness/60Hz/DWM transparency, PCIe ASPM, USB/Wi-Fi power saving, and background throttling) with **automatic snapshot** and optional restore when plugging in the AC charger.
- **Accurate `CPU+iGPU` Laptop Power Telemetry:** detects integrated GPUs (Intel UHD/HD/Iris and AMD Radeon Graphics/Vega/610M–890M) to skip false discrete GPU estimates and clearly label `CPU+iGPU` power draw.
- **Styled Dark System Tray Menu (`TrayPopupMenuWindow`):** custom dark popup menu replacing the legacy white Win32 menu, with live RAM usage header, 1-click **Auto Game Booster**, **Sustained CPU Boost**, **Flush DNS Cache**, RAM cleaners, and **Eco Mode**.
- **Rounded & Detailed Splash Screen:** clean `VisualBrush` rounded clipping for the top accent bar and ambient glow, `[1/4]`–`[4/4]` step badge, and live subsystem initialization chips.

## v3.2.1 (Collapsible Vector Sidebars, Real Program Icons & Fluid Micro-Animations)
- **Collapsible Vector-Icon Navigation Sidebars (MainWindow & Software Installer):** compact `64px` icon-only default view with crisp `24×24` vector icons, smooth `CubicEase` expansion (`64px` ↔ `218px`/`228px`), instant tooltips, and icon hover scale animations.
- **178 Real Official Program Icons:** embedded `32×32` full-color official icons for all catalog apps, decoded in-memory (`0 ms` lag, `100% offline`).
- **Global Fluid Hover Micro-Animations & Payhip API v2:** smooth hover scaling on buttons, dark secondary window frames, masked license key input with reveal toggle, and direct Bug Report button (`optiroder@gmail.com`).

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

