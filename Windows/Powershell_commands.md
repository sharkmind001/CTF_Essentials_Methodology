# Windows PowerShell: Cmdlet vs Alias

PowerShell supports two types of commands:
1. **Alias**: An alternative name for a cmdlet or function (e.g., `copy` is an alias for `Copy-Item`).
2. **Cmdlet**: A built-in PowerShell command (e.g., `Copy-Item`).

- Both work the same, but cmdlets may offer additional functionality.
- PowerShell commands are written in camel case (e.g., `Get-Process`, `Set-Date`).

> ## Basic Commands in PowerShell

| **Command**                                      | **Description**                                            |
|--------------------------------------------------|------------------------------------------------------------|
| `dir /?`                                         | Display help for a command                                 |
| `tasklist /?`                                    | Display help for tasklist command                          |
| `Get-Alias`                                      | List all aliases                                           |
| `get-location`, `pwd`                            | Show current path                                          |
| `dir`, `ls`, `gci`, `Get-ChildItem`              | Show file list                                             |
| `Get-ChildItem -Name`                            | Show content name without detailed info                    |
| `Get-ChildItem -Name -File`                      | Show files only                                            |
| `Get-ChildItem -Name -Directory`                 | Show directories only                                      |
| `cp`, `copy`, `xcopy amit.txt "test"`            | Copy file                                                  |
| `Copy-Item amit.txt "test"`                      | Copy file                                                  |
| `Remove-Item amit.txt`                           | Delete file                                                |
| `mkdir "amit kumar"`                             | Create directory with space                                |
| `New-Item folder1 -ItemType Directory`           | Create a directory                                         |
| `New-Item amit.txt`                              | Create a file                                              |
| `type nul > amit.psd`                            | Create an empty file                                       |
| `cls`, `Clear-Host`                              | Clear terminal window                                      |
| `Get-Command`                                    | Show all commands                                          |

> ## Task Management

| **Command**                                      | **Description**                                            |
|--------------------------------------------------|------------------------------------------------------------|
| `tasklist`                                       | Show running processes                                     |
| `taskkill /pid 1423`                             | Kill a process by PID                                      |
| `Get-Process`                                    | Show running processes                                     |
| `Get-Process notepad | stop process`             | Kill a specific process (e.g., notepad)                    |
| `start-process notepad`                          | Start a new process (e.g., notepad)                        |
| `net start`                                      | Show all running services                                  |
| `net stop "print spooler"`                        | Stop a specific service                                    |
| `Get-Service`                                    | Show all services                                          |
| `Get-Service | where-object {$_.status -eq 'running'}` | Show only running services                                |
| `Stop-Service "wuauserv"`                        | Stop Windows Update service                                |
| `date`, `Get-date`                               | Show current date and time                                 |
| `Get-TimeZone`                                   | Show system timezone                                       |
| `set-Date`                                       | Set date and time                                          |

> ## System Information

| **Command**                                      | **Description**                                            |
|--------------------------------------------------|------------------------------------------------------------|
| `hostname`                                       | Show computer name                                         |
| `$env:COMPUTERNAME`                              | Show computer name (using environment variable)            |
| `msinfo32`, `systeminfo`                         | Show detailed system information                           |
| `Get-computeinfo`                                | Show system information                                    |
| `getmac`, `Get-WmiObject win32_networkadapterconfiguration | Select description, macaddress` | Show MAC address |
| `diskpart`, `Get-volume`                         | Show all volumes                                            |
| `Get-volume -filesystemlabel os`                 | Show information about a volume                            |
| `[System.Environment]::OSVersion.Version`        | Show Windows version                                        |
| `wmic`, `get-wmiobject win32_bios`               | Show BIOS version                                           |
| `history`, `h`, `invoke-history`                 | Show command history                                       |
| `Invoke-History -id 40`                          | Execute a command from history (by ID)                     |

> ## IP Configuration and Networking

| **Command**                                      | **Description**                                            |
|--------------------------------------------------|------------------------------------------------------------|
| `ipconfig`, `Get-NetIpAddress`                   | Show IP address of adapters                                |
| `Get-NetIpConfiguration`                         | Show adapter configuration                                 |
| `tracert`, `Test-NetConnection -TraceRoute www.google.com` | Show route to a website                                  |
| `wmic nic get name`, `Get-Netadapter`            | Show network adapters                                      |
| `netsh wlan show interface`                      | Show WLAN interface details                                |
| `Disable-NetAdapter "Wi-Fi"`                     | Disable Wi-Fi adapter                                      |
| `enable-NetAdapter "Wi-Fi"`                      | Enable Wi-Fi adapter                                       |
| `set-netfirewallProfile -Profile PRIVATE -Enabled False` | Turn off private firewall                                  |
| `set-NetFirewallProfile Profile PUBLIC -Enabled False`  | Turn off public firewall                                  |
| `set-NetFirewallProfile Profile PUBLIC -Enabled True`   | Turn on public firewall                                   |
| `New-NetFirewallRule -DisplayName Amit -Porfile @('public','private') -Direction Inbound -Action` | Create new firewall rule                                  |
| `netsh wlan delete profile name="redmi"`         | Delete a WLAN profile                                      |
| `netsh wlan add profile filename="realme.xml"`   | Add a WLAN profile (stored in XML)                         |

> ## File Encryption and User Management

| **Command**                                      | **Description**                                            |
|--------------------------------------------------|------------------------------------------------------------|
| `cipher /e amit.txt`                            | Encrypt a file                                             |
| `(Get-Item file.txt).Encrypt`                    | Encrypt a file                                             |
| `(Get-Item file.txt).Decrypt`                    | Decrypt a file                                             |
| `(Get-Item file.xml).Attributes='hidden'`        | Hide a file                                                |
| `New-LocalUser`                                  | Create a new local user (follow prompts)                   |
| `Remove-LocalUser`                               | Delete a local user                                        |
| `New-LocalGroup amit`                            | Create a new local group                                   |
| `Remove-LocalGroup amit`                         | Delete a local group                                      |
| `$pass = ConvertTo-SecureString "pass123" -AsPlainText -Force` | Create a secure password for BitLocker                   |
| `Enable-BitLocker -MountPoint D: -EncryptionMethod aes128 -Pin $pass` | Enable BitLocker on a drive                                |
| `Disable-BitLocker`                              | Disable BitLocker                                          |
| `Format-Volume`                                  | Format a drive (follow prompts)                            |
| `Set-Content new.txt 'this is the text'`         | Create a text file with content                            |
| `Restart-computer`                               | Restart the computer                                       |

> ##  PowerShell Scripting

- Variables: Declare variables using `$` sign (e.g., `$a = 2`).
- Data Types: PowerShell supports various data types such as `[int]`, `[char]`, `[double]`.

> ##  Arithmetic Example:
```powershell
$ad = 14
$ds = 56
$fd = $ad * $ds
$fd
```


> ##  Creating Variables
```
$a = 2
$b = 23432.3
[char]$c = 'a'
$d = "Amit Kumar"
```
> ##  To check the data type of variables
```
$a.GetType().Name
$b.GetType().Name
$c.GetType().Name
$d.GetType().Name
```
> ##  Read input from the user
```
[int]$a = Read-Host
```
> ##  Data Types in PowerShell
```
$a = 2
$b = 220.25
[char]$c = 0
$d = "adarsh"
```
> ##  To check the data type
```
$a.GetType().Name
$b.GetType().Name
$c.GetType().Name
$d.GetType().Name
```
> ##  Variables in PowerShell
```
$a
$sun_set
```
> ##  Operators in PowerShell
  1) Assignment
  2) Arithmetic
  3) Logical
  4) Comparison

> ##  Arithmetic Example
```
$ad = 14
$ds = 56
$fd = $ad * $ds
$fd
```
> ##  Assignment Example
```
$ada = 14
$dsa = 56
$fda = $ad -= $ds
$fda
```
> ##  Logical Example
```
$z = 7
$x = 7
($z -ge $x)
```
> ##  Logical Example with Negation
```
$o = 4
$k = 7
($o -gt $k) -! ($o -gt $k)
```
> ##  Calculator Code in PowerShell

```
[int]$a = Read-Host -Prompt 'Enter 1st Number'
[char]$b = Read-Host -Prompt 'Enter Operation You Want (+, -, *, /, %)'
[int]$c = Read-Host -Prompt 'Enter 2nd Number'

[int]$add = $a + $c
[int]$sub = $a - $c
[int]$multiple = $a * $c
[double]$divide = $a / $c
[int]$modulus = $a % $c

switch($b)
{
    + { $result = 'You chose Addition'
        Write-Host("Your answer is $add")
        break
    }
    - { $result = 'You chose Subtraction'
        Write-Host("Your answer is $sub")
        break
    }
    * { $result = 'You chose Multiplication'
        Write-Host("Your answer is $multiple")
        break
    }
    % { $result = 'You chose Modulus'
        Write-Host("Your answer is $modulus")
        break
    }
    / { $result = 'You chose Division'
        Write-Host("Your answer is $divide")
        break
    }
}
$result
Pause
```
> ##  Download & Install Anything Using PowerShell
```
powershell.exe -NoProfile -InputFormat None -ExecutionPolicy AllSigned -Command "[System.Net.ServicePointManager]::SecurityProtocol = 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://dl-cli.pstmn.io/install/win64.ps1'))"
```


