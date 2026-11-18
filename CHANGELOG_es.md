# TorkeToolkit — Historial de Actualizaciones (Changelog)

## v3.2.0 (Versión Consolidada de Lanzamiento)

### Centro de Drivers Oficiales y Descargas Simultáneas
- **Centro de Drivers Sin Windows Update (`DriverCenterWindow`):** escanea CPU, todas las GPUs y controladores clave (`Win32_PnPSignedDriver` + `Win32_Processor` + `Win32_VideoController`), consulta actualizaciones WHQL directamente por HTTP en **Microsoft Update Catalog** y **NVIDIA Official API**, permite selección múltiple en cola con **Seleccionar Todos (Updates)** e instala `.cab` vía `pnputil` con escudo protector para periféricos **INPUT/USB**.
- **Descargas Simultáneas (`1x`–`5x`) y Porcentaje en Vivo:** el Gestor de Software ahora permite elegir cuántas descargas correr en paralelo (`1x` a `5x`) con progreso global agregado (`0%`–`100%`), porcentaje en tiempo real para Winget, Chocolatey, descargas directas, Centro de Drivers y Actualizador.

### Batería, Carga Inteligente y Diagnóstico Preventivo
- **Salud de Batería, Ciclos y Carga Inteligente (`TORKE BATTERY GUARD`):** lectura nativa vía `IOCTL_BATTERY_QUERY_INFORMATION` + WMI (`% de salud`, `desgaste %`, `ciclos de carga`, `mWh` reales vs diseño, voltaje y potencia). Incluye modos **Tope Fijo (60–85%)**, **Horario** y **Adaptativo** (`PowerModeChanged`), adaptadores nativos para **ASUS** (`ATKACPI` + `AsusAtkWmi_WMNB`), **Dell** (`DCIM_BIOSService` WMI + `cctk.exe`), **HP** (`root\HP\InstrumentedBIOS` Battery Health Manager) y **Lenovo** (`EnergyDrv` + `PWRMGRV`), más soporte universal por **Enchufe Inteligente HTTP** y **Alerta en Bandeja**. Disponible desde **Plan 1**.
- **Autodiagnóstico Integral de Fallos (12 Puntos):** detector preventivo automático para espacio crítico en `C:`, alertas S.M.A.R.T., temperaturas elevadas, dispositivos con error en PnP (`ConfigManagerErrorCode`), desgaste de batería, RAM/Pagefile, servicios esenciales detenidos, Windows Update/reinicio pendiente, volcados BSOD recientes (`Minidump`), red/DNS, firewall y runtimes VC++.

### Telemetría en Tiempo Real e Info Hardware
- **Motor Nativo `LibreHardwareMonitorLib`:** lectura en tiempo real de temperaturas reales de CPU, GPU y discos (`°C`), frecuencias (`MHz`), consumo eléctrico total conjunto de la PC (`CPU + RAM RAPL + GPU + Base` / `PSU` / `Batería`), velocidad de red (`↓/↑ KB/s`) y ventiladores (`RPM`).
- **Monitor Renovado (Estilo Torke Lab):** 4 tarjetas KPI con riel lateral de color, osciloscopio en vivo (`CPU / RAM / GPU` con área sombreada), acceso rápido a **Liberar RAM**, **Batería 80%** y **Auditoría Hardware**. Disponible completo desde **Plan 1**.
- **Auditoría de Hardware y Sensores (9 sub-pestañas):** `Resumen` (con Matriz de Salud Torke), `Procesador` (topología de núcleos, cachés, instrucciones AVX/SSE/AES), `Gráfica` (antigüedad de driver y VRAM), `Memoria` (módulos DIMM y canal), `Placa base` (BIOS, VBS, HVCI, TPM, Secure Boot), `Almacenamiento` (discos, volúmenes y TRIM), `Red`, `Windows` y `Sensores (1s)` + exportación de informe sin datos sensibles.

### Gaming Pro, MiniOS X y Personalización
- **+1,000 Juegos y Emuladores en Game Booster:** ampliación masiva de `GameBoosterService` incluyendo emuladores (PCSX2, RPCS3, Dolphin, Cemu, Ryujinx, Yuzu/Suyu, DuckStation, PPSSPP, RetroArch, Xenia, Vita3K, MAME, BlueStacks, LDPlayer, etc.) y más de 1,000 títulos de PC.
- **MiniOS X Personalizable y Portable:** configurador visual con 16 módulos independientes (`MiniOsConfigWindow`), 3 presets rápidos y guardado automático en `minios-profile.json` + Exportar/Importar JSON para llevar tu perfil en USB a cualquier PC.
- **Tema Claro de Alto Contraste:** contraste mejorado en fondos, bordes, barra lateral, consola de operaciones, acentos adaptativos (`TorkeCyan`/`TorkeBlue`) y pestaña Sistema.

### Instalador, Desinstalador, Drivers y Licencias
- **Centro de Drivers y Actualizaciones Oficiales (`DriverCenterWindow`):** escanea hardware local (`Win32_PnPSignedDriver`), consulta actualizaciones reales WHQL desde **Microsoft Windows Update (`Microsoft.Update.Session`)** y **NVIDIA Official API**, abre búsquedas por Hardware ID en **Microsoft Update Catalog**, e instala asistentes OEM verificados vía Winget (`Intel DSA`, `NVIDIA App`, `AMD`, `Dell`, `HP`, `Lenovo`, `ASUS`, `SDIO`, `DDU`, `DriverStore Explorer`) con respaldo DISM previo.
- **Desinstalador Profundo Pro (Estilo Revo):** detección de restos en AppData/Registro/Accesos directos, cierre de procesos bloqueantes, reparación ACL, borrado al reiniciar (`MoveFileEx`), eliminación forzada, lote multi-app, actualización rápida con Winget e **iconos reales locales** asíncronos (0 KB extra en el ejecutable).
- **Instalador Resiliente de +140 Apps:** canales configurables (**Winget / Chocolatey / Directo**) con memoria automática ante fallos, verificación `.part` + SHA-256 / magic-bytes, sección ampliada de drivers y carpeta de descargas persistente.
- **Licenciamiento Tier 3 USB Unificado y KeyGen Privado:** las claves Nivel 3 activan el Modo USB Portable automáticamente con una sola clave, e incorporamos la interfaz privada `TorkeKeyGen.Gui`.

## Versiones anteriores (v3.0.x – v3.1.0 base)
- Arquitectura multiidioma completa (**Español / Inglés**) con validación automática de claves UI.
- Limpiador profundo de shaders/caché, Gestor de Inicio (`StartupManager`), Desinstalador de Bloatware UWP, Conversor/Merge de documentos, Modo Eco en bandeja y Taller Técnico Tier 3 con exportación PDF.

