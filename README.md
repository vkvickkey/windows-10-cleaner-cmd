# windows-10-cleaner-cmd
windows 10 cleaner cmd

You're looking for a way to clean up Windows 10 using the Command Prompt (Cmd). Here are some commands that can help:

**1. Disk Cleanup**


    cleanmgr


:: Remove all temporary files.

    del /f /s /q %tmp%\*.*
#
    del /f /s /q %temp%\*.*
#
    del /f /s /q %systemdrive%\*.tmp
#
    del /f /s /q %systemdrive%\*._mp
#
    del /f /s /q %windir%\temp\*.*
#
    del /f /s /q %AppData%\temp\*.*
#
    del /f /s /q %HomePath%\AppData\LocalLow\Temp\*.*





This command opens the Disk Cleanup tool, which allows you to delete temporary files, system files, and other items you don't need.

**2. System File Checker**

     sfc /scannow

This command scans your system files and replaces any corrupted or missing files.

**3. DISM (Deployment Image Servicing and Management)**

    dism /online /cleanup-image /restorehealth

This command scans your system for corrupted files and replaces them with healthy ones.

**4. Temporary Files**

    del /q /f /s %temp%\*

This command deletes all temporary files in the Temp folder.

**5. Windows Update Cleanup**

    dism /online /cleanup-image /startcomponentcleanup

This command cleans up Windows Update files and frees up disk space.

**6. System Error Logs**

     del /q /f /s %windir%\logs\*

This command deletes system error logs.

**7. Windows Defender Logs**

    del /q /f /s %windir%\system32\wdi\logs\*

This command deletes Windows Defender logs.

**8. Clear DNS Cache**

    ipconfig /flushdns

This command clears the DNS cache.

**9. Clear Windows Store Cache**

    wsreset.exe

This command clears the Windows Store cache.

**10. Disk Defragmentation**

    defrag c: -v -u

This command defragments the C: drive.

Remember to run these commands as an administrator (right-click on the Command Prompt icon and select "Run as administrator") to ensure they work properly.

Please note that some of these commands may require a restart to take effect.

# windows 10 update stop fores

You're looking for ways to stop or pause Windows 10 updates. Here are some methods:

**Method 1: Pause Updates**

1. Go to **Settings** > **Update & Security** > **Windows Update**
2. Click on the **Pause updates** toggle switch to pause updates for up to 35 days

**Method 2: Disable Windows Update Service**

1. Press the **Windows key + R** to open the Run dialog box
2. Type **services.msc** and press Enter
3. In the Services window, find the **Windows Update** service
4. Right-click on it and select **Stop**
5. To prevent the service from starting automatically, right-click on it again and select **Properties**
6. In the Properties window, set the **Startup type** to **Disabled**

**Method 3: Use the Registry Editor**

1. Press the **Windows key + R** to open the Run dialog box
2. Type **regedit** and press Enter
3. Navigate to the following key: `HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\WindowsUpdate\AU`
4. Create a new DWORD (32-bit) value named **NoAutoUpdate** and set its value to **1**
5. Restart your computer

**Method 4: Use the Group Policy Editor**

1. Press the **Windows key + R** to open the Run dialog box
2. Type **gpedit.msc** and press Enter
3. Navigate to the following path: `Computer Configuration` > `Administrative Templates` > `Windows Components` > `Windows Update`
4. Double-click on the **Configure Automatic Updates** policy
5. Select the **

#windows 10 clean virus cmd

You're looking for ways to clean a virus from Windows 10 using the Command Prompt (Cmd). Here are some commands that can help:

**Note:** Before running any of these commands, make sure you have a backup of your important files and data.

**1. Windows Defender Scan**

    powershell -Command "Start-Process -FilePath 'C:\Program Files\Windows Defender\MpCmdRun.exe' -ArgumentList '-Scan -ScanType 3' -Verb RunAs"

This command runs a full scan of your system using Windows Defender.

**2. SFC (System File Checker) Scan**

    sfc /scannow

This command scans your system files and replaces any corrupted or missing files.

**3. DISM (Deployment Image Servicing and Management) Scan**

    dism /online /cleanup-image /restorehealth

This command scans your system for corrupted files and replaces them with healthy ones.

**4. Malware Removal Tool**

    mrt.exe

This command runs the Microsoft Malware Removal Tool, which scans your system for malware and removes it.

**5. Windows Update Cleanup**

    dism /online /cleanup-image /startcomponentcleanup

This command cleans up Windows Update files and frees up disk space.

**6. Temporary Files Cleanup**

    del /q /f /s %temp%\*

This command deletes all temporary files in the Temp folder.

**7. System Error Logs Cleanup**

    del /q /f /s %windir%\logs\*

This command deletes system error logs.

**8. Windows Defender Definitions Update**

    powershell -Command "Start-Process -FilePath 'C:\Program Files\Windows Defender\MpCmdRun.exe' -ArgumentList '-SignatureUpdate' -Verb RunAs"

This command updates Windows Defender definitions.

**9. System Restore**

    systempropertiesprotection

This command opens the System Restore window, where you can select a restore point to revert your system to a previous state.

**10. Reboot in Safe Mode**

    shutdown /r /o /f

This command reboots your system in Safe Mode, which can help you remove malware.

Remember to run these commands as an administrator (right-click on the Command Prompt icon and select "Run as administrator") to ensure they work properly.

Please note that some of these commands may require a restart to take effect.
