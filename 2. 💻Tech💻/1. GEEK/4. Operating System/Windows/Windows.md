# Get Version/Build Number
``` powershell
Get-WmiObject -Class win32_OperatingSystem (| select Version,BuildNumber)
```

Some other useful classes that can be used with `Get-WmiObject` are `Win32_Process` to get a process listing, `Win32_Service` to get a listing of services `Win32_Bios` to get BIOS information. We can use the `ComputerName` parameter to get information about remote computers. `GetWmiObject` can be used to start and stop services on local and remote computers, and more. 


# RDP
#### xfreerdp
``` shell
xfreerdp /v:<targetIp> /u:htb-student /p:Password
```

# Exploring Directories Using Command Line
- dir 
- tree

#  WS01\bob.smith:(OI)(CI)(F)

```cmd-session
C:\htb> icacls c:\windows
c:\windows NT SERVICE\TrustedInstaller:(F)
           NT SERVICE\TrustedInstaller:(CI)(IO)(F)
           NT AUTHORITY\SYSTEM:(M)
           NT AUTHORITY\SYSTEM:(OI)(CI)(IO)(F)
           BUILTIN\Administrators:(M)
           BUILTIN\Administrators:(OI)(CI)(IO)(F)
           BUILTIN\Users:(RX)
           BUILTIN\Users:(OI)(CI)(IO)(GR,GE)
           CREATOR OWNER:(OI)(CI)(IO)(F)
           APPLICATION PACKAGE AUTHORITY\ALL APPLICATION PACKAGES:(RX)
           APPLICATION PACKAGE AUTHORITY\ALL APPLICATION PACKAGES:(OI)(CI)(IO)(GR,GE)
           APPLICATION PACKAGE AUTHORITY\ALL RESTRICTED APPLICATION PACKAGES:(RX)
           APPLICATION PACKAGE AUTHORITY\ALL RESTRICTED APPLICATION PACKAGES:(OI)(CI)(IO)(GR,GE)

Successfully processed 1 files; Failed processing 0 files
```

-   `F` : full access
-   `D` :  delete access
-   `N` :  no access
-   `M` :  modify access
-   `RX` :  read and execute access
-   `R` :  read-only access
-   `W` :  write-only access
-   `(CI)`: container inherit
-   `(OI)`: object inherit
-   `(IO)`: inherit only
-   `(NP)`: do not propagate inherit
-   `(I)`: permission inherited from parent container

# `Server Message Block protocol` (`SMB`)
![[Pasted image 20221007100912.png]]
#### Share permissions

Permission

Description

`Full Control`

Users are permitted to perform all actions given by Change and Read permissions as well as change permissions for NTFS files and subfolders

`Change`

Users are permitted to read, edit, delete and add files and subfolders

`Read`

Users are allowed to view file & subfolder contents

#### NTFS Basic permissions

Permission

Description

`Full Control`

Users are permitted to add, edit, move, delete files & folders as well as change NTFS permissions that apply to all allowed folders

`Modify`

Users are permitted or denied permissions to view and modify files and folders. This includes adding or deleting files

`Read & Execute`

Users are permitted or denied permissions to read the contents of files and execute programs

`List folder contents`

Users are permitted or denied permissions to view a listing of files and subfolders

`Read`

Users are permitted or denied permissions to read the contents of files

`Write`

Users are permitted or denied permissions to write changes to a file and add new files to a folder

`Special Permissions`

A variety of advanced permissions options

# Get-Alias
```powershell-session
PS C:\htb> get-alias

CommandType     Name                                               Version    Source
-----------     ----                                               -------    ------
Alias           % -> ForEach-Object
Alias           ? -> Where-Object
Alias           ac -> Add-Content
Alias           asnp -> Add-PSSnapin
Alias           cat -> Get-Content
Alias           cd -> Set-Location
Alias           CFS -> ConvertFrom-String                          3.1.0.0    Microsoft.PowerShell.Utility
Alias           chdir -> Set-Location
Alias           clc -> Clear-Content
Alias           clear -> Clear-Host
Alias           clhy -> Clear-History
Alias           cli -> Clear-Item
Alias           clp -> Clear-ItemProperty
```

# ExecutionPolicy
```powershell-session
PS C:\htb> Get-ExecutionPolicy -List

        Scope ExecutionPolicy
        ----- ---------------
MachinePolicy       Undefined
   UserPolicy       Undefined
      Process       Undefined
  CurrentUser       Undefined
 LocalMachine    RemoteSigned
```

# wmic

```cmd-session
C:\htb> wmic os list brief

BuildNumber  Organization  RegisteredUser  SerialNumber             SystemDirectory      Version
19041                      Owner           00123-00123-00123-AAOEM  C:\Windows\system32  10.0.19041
```