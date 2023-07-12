### Description : This log in Virtualization is to, Install and Configure Hyper-V Manager on windows

**GetHelp** : [https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/quick-start/enable-hyper-v](https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/quick-start/enable-hyper-v)

## System information and System requirements

GUI - Click Start – RUN , type “msinfo32.exe” and press enter

CLI - PS C:\Users\admin> systeminfo

Find out if Intel VT-x or AMD-V Virtualization Technology is supported in Windows ,

We can go there from **Task Manager** and **Performance Tab**

## Enable the Hyper-V role through Settings

1.  Open Control Panel.
    
2.  Click Programs and Features.
    
3.  Click Turn Windows features on or off or open Start menu, type “optionalfeatures”, and press Enter
    
4.  Expand the Hyper-V section.
    
5.  Check Hyper-V Management Tools box to install Hyper-V Manager
    
6.  Check Hyper-V Platform to enable the Hyper-V role
    

Note : After the installation, a system reboot is required to apply all the changes.

**Version** - From Hyper-V manager , Click on Help and **About Hyper-V Manager**

## Enable Hyper-V using PowerShell

1.  Open a PowerShell console as Administrator.
    
2.  Run the following command:
    

```
PS C:\WINDOWS\system32> Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V -All
```

Note : After the installation, a system reboot is required to apply all the changes.

**Version** - From Hyper-V manager , Click on Help and **About Hyper-V Manager**

## Enable Hyper-V with CMD and DISM

1.  Open up a PowerShell or CMD session as Administrator.
    
2.  Type the following command:
    

```
PS C:\WINDOWS\system32> DISM /Online /Enable-Feature /All /FeatureName:Microsoft-Hyper-V
```

Note : After the installation, a system reboot is required to apply all the changes.

**Version** - From Hyper-V manager , Click on Help and **About Hyper-V Manager**

