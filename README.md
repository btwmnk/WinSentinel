# WinSentinel

A WinUI 3 (Windows App SDK) security & system‑inspection toolkit — a lightweight,
Sysinternals‑style "all‑in‑one" for spotting what's really running on a Windows PC.

> ⚠️ Requires administrator rights. Windows 10/11 x64. For defensive/diagnostic use
> on systems you own or are authorized to inspect.

## Features

- **Mitigations** — per‑process exploit mitigations & IFEO flags (ASLR, DEP, CFG, CPU priority, …).
- **Monitor** — real‑time ETW activity (processes, file, registry, network) with Game / Program / Network modes; captures created‑then‑deleted temp files.
- **Processes** — details view with process **tree**, loaded **modules (DLLs)**, Authenticode signature, hidden‑process detection, VirusTotal lookup.
- **Autoruns** — all persistence points (Run keys, services, drivers, tasks, WinLogon, IFEO, LSA, etc.) with signatures, icons, enable/disable/delete, including Sysinternals `AutorunsDisabled` entries.
- **Connections** — live TCP/UDP (netstat‑style): process → remote endpoint & state, flags unsigned processes talking to the internet.
- **Drivers** — loaded kernel drivers with signature; **install/uninstall a .sys**.
- **Injection** — scans for unbacked executable memory (PRIVATE+EXEC / RWX) — reflective‑DLL / shellcode indicators.
- **Defender** — status (AV / real‑time / tamper protection) and exclusion management (add/remove).
- **Execution** — run history from Prefetch, BAM and UserAssist — see what ran, even if the file is gone.
- **Hosts** — view/edit the hosts file with a safety backup.

## Build

1. Visual Studio 2022 with **.NET 8** and the **Windows App SDK** workload.
2. Open `WinSentinel.sln`, select **x64**, **Build → Rebuild Solution**.
3. Run as administrator.

## Notes

- Unsigned kernel drivers won't load while Driver Signature Enforcement (DSE) is on — that's expected.
- Some artifacts (e.g. BAM) are system‑protected and are accessed via backup/restore privilege.

## Disclaimer

Provided as‑is for security research and system administration. You are responsible
for how you use it. Not affiliated with Microsoft or Sysinternals.
