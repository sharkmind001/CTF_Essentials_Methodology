# Bash Scripting

## Linux Symbols

| Character | Name              | Description                          |
|-----------|-------------------|--------------------------------------|
| `#!/bin/bash` | Shebang (Bang line) | Indicates the script interpreter.  |
| `~`       | Tilde             | Represents the home directory.      |
| `` ` ``   | Backtick          | Used for command substitution.       |
| `!`       | Not               | Logical negation or "bang" operator. |
| `@`       | At the rate       | Used in email addresses, etc.       |
| `#`       | Pound             | Used for comments in shell scripts. |
| `$`       | Dollar            | Represents variables or shell prompt. |
| `%`       | Percentage, Modulo| Modulo operator, or percentage symbol. |
| `^`       | Carat, Circumflex | Used for power or exponentiation.   |
| `&`       | Ampersand         | Used for background processes or conjunction. |
| `*`       | Asterisk          | Wildcard character, or multiplication operator. |
| `-`       | Hyphen            | Used for subtraction, or as a dash. |
| `\|`       | Pipe, Bar         | Redirects output from one command to another. |
| `.`       | Period            | Used to indicate the current directory or file extension. |
| `\`       | Escape            | Escapes special characters.        |
| `<` `>`   | Angle Brackets    | Used for input and output redirection. |


## Print Function:
```
printf "hello I am sudhir" or 
echo "Hello I am sudhir"
echo -e "today date is \c";date         //to print same line
```
## Variable:

**Note.: **
if you make variable always use $ sign and no space between variable and value.

For example
```
user=$(whoami)
ip=$(seq 50 100)
```
**Note.2:**
To use any bash function to globally use then you have to make .bash_profile file in home directory.
although you can make any named file using .file_name










































