
#hack  #batch  #information_collection

```batch
@echo off

::Displays detailed configuration information about a computer and its operating system,
::including operating system configuration, security information, product ID,
::and hardware properties (such as RAM, disk space, and network cards).
systeminfo

::Displays a list of currently running processes on the local computer or on a remote computer

tasklist


::Displays WMI information inside an interactive command shell.

wmic context


echo %processor_architecture%


netstat

:: Displays the Resultant Set of Policy (RSoP) information for a remote user and computer. To use RSoP reporting for remotely targeted computers through the firewall, you must have firewall rules that enable inbound network traffic on the ports.

gpresult /z 

ipconfig /all



```