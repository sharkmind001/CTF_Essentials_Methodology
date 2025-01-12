# Data Filteration using terminal

> ## Read Files( cut, wc, tee)

| Command           | Description                                      |
|-------------------|--------------------------------------------------|
| `cat -n file.txt` | Open file on terminal                            |
| `tac file.txt`    | It is cat in inverse mode                        |
| `wc -l -c -w`     | Used to count lines, characters, and words       |
| `tee`             | Save with show output                           |
| `tee -a`          | Save without overwriting previous data (append) |

> ## CUT command
```
cut <options> file

cut -c5 /etc/passwd
cut -c1-5 /etc/passwd

```

| Option | Use                                  |
|--------|--------------------------------------|
| `-c`   | Character                            |
| `-d`   | Delimiter: `/`, `:`, `a`, `b`, etc. |
| `-f`   | Fields: `1`, `2` or range `1-5` column-wise |

```
cat /etc/passwd | cut -d':' -f1 
cat /etc/passwd | cut -d'/' -f1-5 
```

> ## HEAD & TAIL command:
 ```
head -1 /etc/passwd
head -n 5 /etc/passwd
tail -3 /etc/passwd
tail -n 7 /etc/passwd
 ```
> ## SORT and UNIQ command

| Command                                      | Description                                              |
|----------------------------------------------|----------------------------------------------------------|
| `sort file.txt`                              | Arranges columns alphabetically in ascending order       |
| `sort -k2 file.txt`                          | Arranges based on the 2nd column                         |
| `sort -n -k4 file.txt`                       | Arranges numeric items in ascending order                |
| `ls /bin /usr/bin \| sort \| uniq -d`        | Shows only repeated words                                 |
| `ls /bin /usr/bin \| sort \| uniq -c`        | Shows how many times an item is repeated                  |


> ## (tr) TRANSLATE COMMAND

| Command                              | Description                                      |
|--------------------------------------|--------------------------------------------------|
| `cat /etc/passwd \| tr 'a' 'A'`      | Translates `a` to `A`                           |
| `cat /etc/passwd \| tr 'a-z' 'A-Z'`  | Translates all characters to uppercase          |
| `kill -l \| tr ' ' '\n'`             | Changes spaces to new lines                     |
| `cat /etc/passwd \| tr '\n' ' '`     | Changes new lines to spaces                     |
| `cat /etc/passwd \| tr -d a`         | Removes a particular character like `a`         |

> ## ROT13(rotation 13) encryption

| Command                                          | Description                                      |
|--------------------------------------------------|--------------------------------------------------|
| `cat /etc/passwd \| tr 'a-z' 'nopqrstuvwxyzabcdefghijklm'` | Encrypts using ROT13 (a-m, n-z)                   |
| `cat /etc/passwd \| tr 'a-z' 'n-za-m'`           | Encrypts using ROT13                               |
| `cat /etc/passwd \| tr 'n-za-m' 'a-z'`           | Decrypts the previously encrypted content         |


> ## COMM (comparation command)
 
**Note.:** All file should be sorted before run comm command.


| Command                                      | Description                                              |
|----------------------------------------------|----------------------------------------------------------|
| `comm file1 file2`                           | Compares two files and shows the result in 3 columns. The 1st column shows unique lines from `file1`, the 2nd from `file2`, and the 3rd shows common lines. |
| `comm -12 file1 file2`                       | Excludes the 1st and 2nd columns of the result and only prints the 3rd column (common lines). |


> ## Access Control List(ACL)
 
ACL comes to protect files & directories.
 
It is two types 
 
  1.	Acesses ACL: It is use individual file or directory.
  2.	Default ACL: It is use only directory.
 
ACL management command ...

| Command  | Description                            |
|----------|----------------------------------------|
| `chacl`  | Change ACL (Access Control List) permission |
| `getfacl`| See ACL (Access Control List) permission  |
| `setfacl`| To set ACL (Access Control List) permission |

> ## GREP command

- `grep -E 'root|games' /etc/passwd`
- `egrep 'root|games|' /etc/passwd /etc/group`
- `grep -w 'root' /etc/passwd`
- `grep -i root /etc/passwd`
- `grep -R root /etc/`
- `grep root /etc/*`
- `grep -A2 /etc/passwd`
- `grep -B3 /etc/passwd`
- `grep -C5 /etc/passwd`
- `grep ^[#] /etc/passwd`
- `grep ^[^#] /etc/passwd`



| `-v`   | Invert match                             |
| `-i`   | To ignore case                           |
| `-c`   | To count occurrences                     |
| `-v`   | Invert matching                          |
| `-n`   | Print line numbers                       |
| `-o`   | Only matching part of the line           |
| `-w`   | For exact word match                     |
| `-E`   | For multiple word search (extended regex)|
| `-R`   | For recursion in directories             |
| `-w`   | For exact word match (duplicate)         |

`cat /etc/passwd | grep -w root `

> ## AWK command
 ```
df -h | awk '{print $1,$4}' | column -t 

```

| `'{print $1}'`  | Field 1                     |
| `-F`            | Delimiter                   |
| `OFS`           | Output Field Separator      |

```
df -h | awk -F'%' '{print $1,$2}'
 
ifconfig | grep -w inet | awk '{print $2}' OFS='  abc  '| column -t

```












