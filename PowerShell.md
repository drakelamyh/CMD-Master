# PowerShell #

| Description | Command |
| -------- | -------- |
| Displays host name portion of the full computer name | `hostname` |
| WMI get serial number of computer | `Get-CimInstance Win32_Bios \| Select-Object -ExpandProperty SerialNumber` |
| Returns media access control (MAC) address and list of network protocols associated with each address for all network cards, either locally or across a network | `getmac` |

