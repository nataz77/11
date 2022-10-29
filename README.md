# Awesome Windows 11

A bunch of tools to make Windows 11 more stylish and powerful.

Pull requests with additional tools and projects are more than welcome!

## Styling and theming
- [Auto Dark Mode](https://github.com/AutoDarkMode/Windows-Auto-Night-Mode): Automatically switches between the dark and light theme of Windows 10 and Windows 11.
- [RoundedTB](https://github.com/torchgm/RoundedTB): Adds margins, rounded corners and segments to the taskbar. 
- [Mica For Everyone](https://github.com/MicaForEveryone/MicaForEveryone): a tool to enable backdrop effect on titlebar of win32 apps on Windows 11 
- [AcrylicMenus](https://github.com/krlvm/AcrylicMenus): Acrylic effect for all existing Win32 context menus 
- [AccentColorizer](https://github.com/krlvm/AccentColorizer): Recolorize Win32 controls in-memory with accent color without patching theme
- [BeautySearch](https://github.com/krlvm/BeautySearch): Windows 10+ Search Window appearance tweaker
- [Dynamic Theme](https://apps.pinnula.fr/en/dynamic-theme/9bghzk): Dynamic background and/or lock screen picture with daily Bing or Windows Spotlight pictures, one Bing or Windows Spotlight picture or personal pictures.
- [Rectify Winver](https://github.com/rounk-ctrl/Winver): Modern fluent design winver application that uses the latest Windows 11 design features.

## Tools
- [Modern Flyouts](https://github.com/ModernFlyouts-Community/ModernFlyouts): A modern Fluent Design replacement for the old Metro themed flyouts present in Windows. 
- [QuickLook](https://github.com/QL-Win/QuickLook): Bring macOS “Quick Look” feature to Windows 
- [EarTrumpet](https://github.com/File-New-Project/EarTrumpet): Volume Control for Windows
- [NanaZip](https://github.com/M2Team/NanaZip): The 7-Zip derivative intended for the modern Windows experience
- [Files](https://files.community): Files is a file manager for Windows with a powerful yet intuitive design.
- [ViVeTool](https://github.com/thebookisclosed/ViVe): C# library and console app for using new feature control APIs available in Windows 10 version 2004 and newer
- [FluentFlyouts3](https://github.com/FireCubeStudios/FluentFlyouts3): Fluent Flyouts 3 WinUI 3 Edition 
- [Shell](https://github.com/moudey/Shell): Powerful context menu manager for Windows File Explorer 
- [ElevenClock](https://github.com/martinet101/ElevenClock): Customize Windows 11 taskbar clock 
- [

## Windows fundamentals
- [LockHunter](https://lockhunter.com/): foolproof file unlocker
- [SysInternals Suite](https://apps.microsoft.com/store/detail/sysinternals-suite/9P7KNL5RWT25): Sysinternals Suite is a bundle of the Sysinternals utilities including Process Explorer, Process Monitor, Sysmon, Autoruns, ProcDump, all of the PsTools, and many more.
- [Clink](https://github.com/chrisant996/clink): Bash's powerful command line editing in cmd.exe 
- [Terminal](https://github.com/microsoft/terminal): Windows Terminal 

## Networking
- [PortMaster](https://github.com/safing/portmaster): free and open-source application firewall that does the heavy lifting for you.
- [Wireshark](https://github.com/wireshark/wireshark): network traffic analyzer

## Firefox & Windows 11
- [Wavefox](https://github.com/QNetITQ/WaveFox): Windows 11 Mica effect for Firefox
- [EdgeFrfx](https://github.com/bmFtZQ/edge-frfox): A Firefox userChrome.css theme that aims to recreate the look and feel of the Chromium version of Microsoft Edge. 
- [Firefox-UWP-Style](https://github.com/Guerra24/Firefox-UWP-Style): MDL2 + Sun Valley Theme for Firefox 

## Media
- [Open Video Downloader](https://github.com/jely2002/youtube-dl-gui): cross-platform GUI for youtube-dl made in Electron and node.js

## Updates & custom images
- [UUPMediaCreator](https://github.com/gus33000/UUPMediaCreator): An utility to create Windows Media files (.ISO, .WIM, .VHD) from Unified Update Platform files 

## Debloating
There's a bunch of tools out here on GitHub to supposedly debloat Windows 10/11. <br/>
I never had a great experience with those, most of the times they landed me with a broken installation but the side effects were not worth it. Even reverting back the changes did not restore the previous system state, so I rather use this simple poweshell to remove unwanted apps that come preinstalled:
```poweshell
$Apps = @(
    #enter PackageFullNameHere
)
foreach ($App in $Apps) {
        Write-Verbose -Message ('Removing app: {0}' -f $App)
        Get-AppxPackage -Name $App | Remove-AppxPackage -ErrorAction SilentlyContinue
}
```
**NB: this script is just an example and will do nothing as is, [I do NOT take responsibility for what may happen to your system! Run scripts at your own risk!](LICENSE)**
