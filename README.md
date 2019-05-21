﻿# Get-ComputerInfo
USAGE:

Import-Module activedirectory
. .\Get-ComputerInfo.ps1
$Servers = Get-ADComputer -Filter { OperatingSystem -Like '*Windows Server*' } | Select Name
Get-ComputerInfo $Servers.Name | Export-Csv -NoTypeInformation -UseCulture -Path ./server-info.csv
