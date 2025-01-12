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



| Option | Description                              |
|--------|------------------------------------------|
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

| Command         | Description                 |
|-----------------|-----------------------------|
| `'{print $1}'`  | Field 1                     |
| `-F`            | Delimiter                   |
| `OFS`           | Output Field Separator      |


```
df -h | awk -F'%' '{print $1,$2}'
 
ifconfig | grep -w inet | awk '{print $2}' OFS='  abc  '| column -t

```

> ## SED command

| Command                              | Description                          |
|--------------------------------------|--------------------------------------|
| `rename 's/-/./' *`                  | For bulk rename                      |
| `rename 's/-/./' *.txt`              | If your files have a `.txt` extension |

```
ifconfig | grep -w inet | awk '{print $2}' | sed 's/inet/My ip is = /'

```

| Command                    | Description                                        |
|----------------------------|----------------------------------------------------|
| `s`                         | Substitute or replace                             |
| `sed -n '1p;5p'`            | Print 1st and 5th lines                           |
| `sed -n '1,5p'`             | Print lines from 1 to 5                           |
| `sed -n '1p;$p'`            | Print the first and last line                     |
| `sed '5,7d'`                | Delete lines 5 to 7                               |
| `sed '4!d'`                 | Invert delete (delete all except the selected line)|
| `sed '4i amit'`             | Insert the line `amit` after line 4               |
| `sed '7a amit'`             | Insert the line `amit` before line 7              |
| `^`                         | Beginning of the line                             |
| `$`                         | End of the line                                   |
| `-i`                        | Insert in the original file                       |
| `g`                         | Perform substitution globally                     |
| `gi`                        | Perform substitution globally and ignore case     |


| Command                                                        | Description                                                 |
|----------------------------------------------------------------|-------------------------------------------------------------|
| `cat opensea.txt \| sed 's+-+://+'`                             | Replaces `/` with `://`                                     |
| `cat /etc/passwd \| sed -n '1,4p'`                              | Prints lines 1 to 4                                          |
| `cat /etc/passwd \| sed -n '4p;7p;12,17p'`                      | Prints lines 4, 7, and 12 to 17                              |
| `cat /etc/passwd \| sed -n '1p;$p'`                             | Prints the first and last lines                              |
| `cat /etc/passwd \| sed -i 's/root/admin/g'`                    | Replaces `root` with `admin` globally and modifies the file  |
| `cat /etc/passwd \| sed 's/root/admin/gi'`                      | Replaces `root` with `admin`, globally and case-insensitively|
| `cat /etc/passwd \| sed '4s/^/#/'`                              | Adds `#` at the beginning of line 4                         |
| `cat /etc/passwd \| sed 's/$/.mp4/'`                            | Appends `.mp4` at the end of each line                      |
| `cat /etc/passwd \| sed '2s/root/admin/g'`                      | Replaces `root` with `admin` starting from line 2            |
| `cat /etc/passwd \| sed -e '2s/root/admin/g' -e 's/root/admin/g'`| Runs two `sed` commands in sequence                          |
| `cat /etc/passwd \| sed '2s/root/admin/g;s/root/admin/g'`       | Another way to run two `sed` commands in sequence            |


> ## FIND COMMAND:
 ```
find <location> -<option> <file_type> 

```

| Command                                                      | Description                                                 |
|--------------------------------------------------------------|-------------------------------------------------------------|
| `find / -type f`                                              | Searches all files related to root                          |
| `find / -type d \| wc -l`                                     | Searches all directories related to root                    |
| `find / -empty \| wc -l`                                      | Searches all empty files related to root                    |
| `find / -group gp1`                                           | Shows all files and directories from the `gp1` group        |
| `find / -user user1`                                          | Shows all files related to `user1`                          |
| `find / -iname file`                                          | Searches for files named `file` (case-insensitive)          |
| `find / -nonuser`                                             | Finds files that do not belong to any user                  |
| `find / -size 1M`                                             | Finds files exactly 1MB in size                             |
| `find / -size +1M`                                            | Finds files greater than 1MB in size                        |
| `find / -size -1M`                                            | Finds files smaller than 1MB in size (use `G` for GB, `T` for TB)|
| `find / -type f -name "*.jpg" -size 2M`                        | Finds all `.jpg` files that are exactly 2MB in size         |
| `find / -perm -0400`                                          | Finds files with specific permissions                        |


> ## FIND WITH OPERATORS:

| Command                                                      | Description                                                 |
|--------------------------------------------------------------|-------------------------------------------------------------|
| `find . -name "*.txt" -and -type d`                           | If any part of the command is wrong, it will not execute     |
| `find . -name "*.txt" -a -type d`                             | These two are the same as the previous one                   |
| `find . -iname "*.jpg" -type l`                               | Finds symbolic links for `.jpg` files (default operator used if none specified) |

**Note.:** If we are not defined then it is find in current path "." 

| Command                                                        | Description                                                        |
|----------------------------------------------------------------|--------------------------------------------------------------------|
| `find -name "file*" -or -type d`                                | Finds files named "file*" or directories                           |
| `find -name "file*" -not -type d`                               | Finds "file*" that are not directories (all except directories)    |
| `find . -name "file*" -and -not -type f`                        | Finds "file*" that are not regular files                           |
| `find . -name "*.txt" -o -name "*.jpg" -and -type f`            | Searches for `.txt` or `.jpg` files that are regular files        |
| `find . \( -name "*.txt" -type f \) -or -type d`                | Searches for `.txt` files (and regular files) or directories (using parentheses for grouping) |

**Note.:** Simple linux have "or" operator draw back then it is treat as and operator but mac unix is POSTIX IEEE standardlize.

| Command                                                | Description                                                   |
|--------------------------------------------------------|---------------------------------------------------------------|
| `find -name "file*" , -name "*.txt"`                    | The `,` operator returns the last command value (executes both conditions sequentially) |

```
find . \( -type f -not -perm 0600 \) -or \( -type d -not -perm 0700 \)

```

> ## FIND WITH ACTION
 
These are two types. 
 
   1.	Predefine actions
   2.	User defined actions
 

| Command                                                | Description                                                   |
|--------------------------------------------------------|---------------------------------------------------------------|
| `find . -type f -name "*.mp3" -print`                   | Default action: prints the paths of `.mp3` files               |
| `find . -type f -name "*.mp2" -print0`                  | Prints the paths of `.mp2` files with a null separator (`-print0`) |
| `find . -type f -name "*.mp3" -delete`                  | Deletes the `.mp3` files found                                 |


> ## USER DEFINED ACTIONS:


| Command                                                       | Description                                                     |
|---------------------------------------------------------------|---------------------------------------------------------------|
| `-exec command {} ;`                                           | `{}` holds the output, `;` is the delimiter indicating the end of the command |
| `find . -type f -name "*.mp4" -exec ls -l {} \;`               | Executes `ls -l` on each `.mp4` file found (custom long listing) |
| `find . -type f -name "*.mp4" -exec ls -l {} +`                | Executes `ls -l` on all `.mp4` files at once (using `+` for efficiency) |


In upper snerio \; use find and list in many line by line that is use more ram and cpu usage.
 
In lower snerio + first it will find then in one time list all entities.

It is ask first before execution.
```
find . -type f -nmae "*.mp4" -ok ls -l {} \;	
 ```
```
find / -perm -u=s -type f 2>/dev/null
 
find / -perm -g=s -type f 2>/dev/null
 
find / -perm -g=s -o -perm -u=s -type f 2>/dev/null
 
find /home -writable -type d 2>/dev/null
 
cp $(find  /usr/share/backgrounds -type f -name "*.png") /home/kali/Pictures
```

> ## SYSTEMCTL: 

| Command     | Description                |
|-------------|----------------------------|
| `pstree`    | To show running services tree |
| `pidof`     | To check process ID        |

```
systemctl <action> <service_name>
 ```
```
systemctl status ssh
 ```
```
systemctl start|stop|is-enable|is-active|enable|disable|reload|restart <service_name>

```

| Command                                          | Description                                                    |
|--------------------------------------------------|----------------------------------------------------------------|
| `systemctl list-units`                           | Shows all running services                                     |
| `systemctl`                                      | Shows all services                                             |
| `systemctl \| grep ssh`                           | Displays information about the `ssh` service                   |
| `systemctl list-unit-files`                      | Lists all unit files (services, targets, etc.)                 |
| `systemctl mask \|unmask <service_name>`            | Used for security purposes: in mask mode, the service cannot be started |


> ## CURL (downloading files)

| Command                                                                  | Description                                                      |
|--------------------------------------------------------------------------|------------------------------------------------------------------|
| `curl -O https://www.filedownload.com/file.iso`                           | To download any file                                            |
| `curl -C - -O https://www.filedownload.com/file.iso`                      | To resume a download (using `-C` for continuous)                 |
| `curl --limit-rate 40k -O http://www.example.com/file.iso`                | Set download speed limit (in `b`, `k`, `m`, `g`, `t` for units)   |
| `curl -I www.google.com`                                                  | To view the headers of a request                                 |
| `curl --request POST --data "username" "password" https://www.google.com/`| Send data (e.g., username and password) to a URL                 |
| `curl -o <file_name> www.google.com`                                      | To save the request's output in a specified file                 |
| `curl -I www.google.com \> yahoo.com`                                     | To run a multiline command                                      |
| `curl -L google.com`                                                     | Auto-follow redirections                                         |
| `curl -A <user-agent_name> google.com`                                    | Change the user agent string                                     |
| `curl -A "Mozilla/5.0 (X11; Linux x86_64; rv:91.0) Gecko/20100101 Firefox/91.0" google.com` | Change the user agent string to a specific browser               |
| `curl -x 127.0.0.1:8080 google.com`                                      | Use a proxy (`-x` option)                                        |
| `curl -U username:password -x 127.0.0.1:8080 google.com`                | Access a password-protected proxy                               |
| `curl --cookie "name=value" https://www.google.com`                       | Set cookies for the request                                      |
| `curl -u username:password ftp://ftp.example.com/file.txt`               | Download a file from an FTP server with authentication           |
| `curl -T file_name username:password ftp://ftp.example.com/`             | Upload a file to an FTP server with authentication               |


> ## Curl long commnad:(It is a single command)

```
curl -i -s -k -X $'POST' \
>   -H $'Host: api.amplitude.com' -H $'User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:91.0) Gecko/20100101 Firefox/91.0'
 -H $'Accept: */*' -H $'Accept-Language: en-US,en;q=0.5' -H $'Accept-Encoding: gzip, deflate' 
-H $'Referer: https://opensea.io/' -H $'Content-Type: application/x-www-form-urlencoded; charset=UTF-8' 
-H $'Cross-Origin-Resource-Policy: cross-origin' -H $'Content-Length: 4477' -H $'Origin: https://opensea.io' 
-H $'Sec-Fetch-Dest: empty' -H $'Sec-Fetch-Mode: cors' -H $'Sec-Fetch-Site: cross-site' -H $'Te: trailers' -H $'Connection: close' \
>   --data-binary $'checksum=c4a1a5591a029fb16d3474d1e4d08f3c&client=ddd6ece4d5ddebbf244a249703c9d662&e=%5B%7B%22device_id%22%
3A%22OhcSrn5rHcEGdv-XCc5ePa%22%2C%22user_id%22%3Anull%2C%22timestamp%22%3A1656570191480%2C%22event
```

> ## WGET ( FOR DOWNLOADING FILES):

| Command                                                                 | Description                                                       |
|-------------------------------------------------------------------------|-------------------------------------------------------------------|
| `wget https://www.example.com`                                           | To download a single file                                         |
| `wget -i urls.txt`                                                      | To download multiple files from `urls.txt`                        |
| `wget -r http://www.example.com/dist`                                   | To download all files in the directory index                      |
| `wget -P <YOUR-PATH> https://example.com/sitemap.xml`                    | Download a file to a specific output directory                     |
| `wget -O <YOUR-FILENAME.html> https://example.com/file.html`            | Rename downloaded file when retrieving with `wget`                 |
| `wget --user-agent=Chrome https://example.com/file.html`                 | Define a custom user agent in `wget`                               |
| `wget --user-agent="Mozilla/5.0 (Linux; Android 6.0.1; Nexus 5X Build/MMB29P) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/86.0.4240.198 Mobile Safari/537.36 (compatible; Googlebot/2.1; +http://www.google.com/bot.html)" https://example.com/path` | Extract as Googlebot with `wget`                                    |
| `wget --tries=10 https://example.com`                                    | Define the number of retry attempts in `wget`                      |
| `wget -c https://example.com`                                           | Continue interrupted downloads with `wget`                         |
| `wget --recursive --page-requisites --adjust-extension --span-hosts --wait=1 --limit-rate=10K --convert-links --restrict-file-names=windows --no-clobber --domains example.com --no-parent example.com` | Using `wget` to extract an entire site (Proceed with caution)      |
| `wget --spider -r https://example.com -o wget.log`                       | Run spider mode and log the output (`-o` for output log)          |


| Option                                   | Description                                                   |
|------------------------------------------|---------------------------------------------------------------|
| `--recursive`                            | Follow links in the document (maximum depth is 5)             |
| `--page-requisites`                      | Get all assets (CSS/JS/images)                                |
| `--adjust-extension`                     | Save files with `.html` at the end                             |
| `--span-hosts`                           | Include necessary assets from offsite as well                 |
| `--wait=1`                               | Wait 1 second between extractions                             |
| `--limit-rate=10K`                       | Limit the download speed (bytes per second)                   |
| `--convert-links`                        | Convert the links in the HTML so they still work locally      |
| `--restrict-file-names=windows`          | Modify filenames to work in Windows                           |
| `--no-clobber`                           | Avoid overwriting existing files                              |
| `--domains example.com`                  | Do not follow links outside the `example.com` domain          |
| `--no-parent`                            | Do not ascend to the parent directory when retrieving recursively |
| `--level`                                | Specify the depth of crawling (use `inf` for infinite depth)   |










