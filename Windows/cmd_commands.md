# CMD Commands

| **Command/Function**                                           | **Description**                                                                                             |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| `ctrl + r`                                                     | Type command                                                                                                 |
| `ctrl + shift + enter`                                         | Open cmd with administrator privileges                                                                      |
| `dir /?`                                                       | Help for any command                                                                                         |
| `tasklist /?`                                                  | Help for any command                                                                                         |
| `md amit`                                                      | Make folder                                                                                                  |
| `mkdir amit`                                                   | Make directory                                                                                                |
| `rmdir amit`                                                   | Delete directory                                                                                              |
| `copy cmdnotes.txt "test"`                                     | Copy file                                                                                                     |
| `copy *.txt "test"`                                            | Copy multiple files                                                                                          |
| `del cmdnotes.txt`                                             | Delete file                                                                                                   |
| `move cmdnotes.txt "test"`                                     | Move file                                                                                                     |
| `ren cmdnotes.txt cmd.txt`                                     | Rename file                                                                                                   |
| `rem amit sumit`                                               | Rename folder                                                                                                 |

> ## Findstr

| **Command/Function**                                                              | **Description**                                                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| `systeminfo \| findstr /C:"processor"`                                             | Find a string                                                                                             |
| `systeminfo \| findstr "processor"`                                                | Find a string (default behavior)                                                                          |
| `findstr /bi /F:"processor"`                                                      | Find a file                                                                                               |
| `findstr /bi /D:"processor"`                                                      | Find a directory                                                                                          |
| `systeminfo \| findstr /b "processo"`                                              | Automatically complete remaining word matching the given word                                              |
| `systeminfo \| findstr /i "ProCessor"`                                             | Bypass case sensitivity                                                                                    |
| `systeminfo \| findstr /bi "ProCess"`                                             | Bypass case sensitivity and matching word                                                                 |
| `findstr "computer help" myfile.txt`                                               | Find in a specified text file                                                                              |
| `findstr /s "computer help" *.txt`                                                 | Find in current and all subdirectories                                                                    |
| `findstr /s /x "computer help" *.txt`                                              | Find exact match in current and all subdirectories                                                       |
| `findstr /x /c:"computer help" *.*`                                                | Find exact match across all files                                                                          |
| `findstr /s "KB.." *.txt`                                                         | Find any word matching the pattern in `.txt` files                                                       |






















