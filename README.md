# WinUpdate Commander

A standalone Windows Update management tool with a graphical interface. Search, install, hide, and control updates without using the Settings app. Supports Windows 7 SP1 through Windows 11.

## Features

- Scan for available updates from Microsoft Update (includes drivers, optional updates, and security patches)
- Install selected or all updates with a single click
- Create a system restore point before installation (optional)
- Auto-reboot option after updates complete
- Hide problematic updates to prevent them from being offered again
- View and restore previously hidden updates
- Browse installed update history (last 200 entries)
- Set Delivery Optimization bandwidth limits
- Toggle metered connection status for active network profiles (Windows 8+)
- Purge the Windows Update cache (SoftwareDistribution and catroot2)
- Schedule a weekly automatic update task (runs silently every Sunday at 3:00 AM)
- Toggle between dark and light themes

## Requirements

- Windows 7 SP1, 8, 10, or 11 (32-bit or 64-bit)
- .NET Framework 4.7.2 or later (already included on fully updated Windows 10/11; available as an optional update on Windows 7 SP1)
- Administrator privileges (the tool will request elevation on launch)

## Usage

### Pre-built executable

1. Download `WinUpdateCommander.exe` from the [Releases](https://github.com/auratech0/winupdate-commander/releases) page.
2. Run it. If prompted by User Account Control, allow the elevation.
3. Use the tabs to search, install, hide updates, or configure automation.

### Running from source

If you prefer to build it yourself:

1. Save `WinUpdateCommander.cs` to a folder.
2. Open a command prompt in that folder.
3. Compile with the .NET Framework C# compiler (included with the framework):

   ```cmd
   C:\Windows\Microsoft.NET\Framework64\v4.0.30319\csc.exe /target:winexe /reference:System.dll /reference:System.Drawing.dll /reference:System.Windows.Forms.dll /reference:System.Management.dll /reference:System.ServiceProcess.dll /reference:Microsoft.CSharp.dll /reference:System.Core.dll /out:WinUpdateCommander.exe WinUpdateCommander.cs
