WindowsGSM.SCPSL - MeFriendos build
Version 0.1.1

INSTALL
=======
1. Copy the complete SCPSL.cs folder into:
   <WindowsGSM>\plugins\SCPSL.cs\

2. Reload plugins or restart WindowsGSM.

3. Add "SCP: Secret Laboratory Dedicated Server" and click Install.
   SteamCMD App ID: 996560
   SteamCMD login: anonymous

4. Keep the default Server Port 7777 unless you intentionally use another UDP port.

5. First start / EULA:
   The plugin does NOT auto-accept Northwood's EULA.
   Read the EULA and accept it through LocalAdmin yourself.
   If you have already reviewed and accepted it and intentionally want non-interactive
   startup, LocalAdmin V2 also supports its own --acceptEULA option.

6. Server configuration is stored outside the WindowsGSM instance at:
   %APPDATA%\SCP Secret Laboratory\config\<port>\

   Main file:
   config_gameplay.txt

7. For manual port rules, turn Auto Firewall off in WindowsGSM and create a narrow rule for the selected UDP port.
   Default: 7777/UDP
   Do not create a broad application allow rule for LocalAdmin.exe or SCPSL.exe.

FIREWALL
========
Firewall management follows WindowsGSM's per-server Auto Firewall setting.
The plugin does not create, remove or inspect firewall rules and does not block startup for a plugin firewall check.

Use MeFriendos WindowsGSM v1.25.3.0 with Auto Firewall:
https://github.com/PapaGordon/WindowsGSM/releases/tag/v1.25.3.0
For manual port rules, turn Auto Firewall off for this server in WindowsGSM and configure the required ports yourself. Router forwarding remains separate.

NOTES
=====
- WindowsGSM's Server Name field does not directly set SCP:SL's public server name.
  Set server_name in config_gameplay.txt.
- Default max_players is currently 20 in Northwood's gameplay config.
- LabAPI is bundled with current SCP:SL Dedicated Server builds.
- Server Start Param is for LocalAdmin V2 arguments. Do not put the port there;
  WindowsGSM passes Server Port as LocalAdmin's first positional argument.
- When Embed Console is enabled, the plugin adds:
    --printStd --noSetCursor --disableTrueColor
  unless you already supplied those flags.
- The default plugin parameter is:
    --useDefault
  This avoids the LocalAdmin configuration wizard when no LocalAdmin config exists.
- The plugin does not automate server verification or acceptance of community guidelines.
