### Commands to Spawn a Shell Using Different Methods

| Command                                      | Description                                        |
|----------------------------------------------|----------------------------------------------------|
| `python -c 'import pty; pty.spawn("/bin/sh")'` | Spawn a shell using Python's `pty` module          |
| `python -c 'import pty; pty.spawn("/bin/bash")'` | Spawn a bash shell using Python's `pty` module     |
| `python3 -c "__import__('pty').spawn('/bin/bash')"` | Another way to spawn a bash shell using Python 3  |
| `python3 -c "__import__('subprocess').call(['/bin/bash'])"` | Spawn a bash shell using Python 3's subprocess module |
| `echo 'os.system("/bin/bash")'`              | Use `echo` to execute a bash shell via os system call |
| `sh /bin/sh -i`                              | Start an interactive shell using `/bin/sh`         |
| `bash /bin/bash -i`                          | Start an interactive bash shell                    |
| `perl -e 'exec "/bin/sh";'`                  | Spawn a shell using Perl                           |
| `perl -e 'print `/bin/bash`'`                | Spawn a bash shell using Perl                      |
| `:!bash`                                     | Execute a shell command within `vi` or `vim`       |
| `ruby: exec "/bin/sh"`                       | Spawn a shell using Ruby                           |
| `lua: os.execute('/bin/sh')`                 | Spawn a shell using Lua                            |
