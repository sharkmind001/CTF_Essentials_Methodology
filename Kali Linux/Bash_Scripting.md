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
echo -e "today date is \c";date         #To print same line
```
## Variable:

**Note.:**
if you make variable always use $ sign and no space between variable and value.

For example
```
user=$(whoami)
ip=$(seq 50 100)
```
**Note.2:**
To use any bash function to globally use then you have to make .bash_profile file in home directory.
although you can make any named file using .file_name

**Ex.**
```
nano .abc
a(){
echo "this is test"
}
source .abc
```
## Local variable
```
name=Amit

echo $name
```
## Global variable
```
export mob=788744774

echo $mob
```
## How to use reserve variable
```
dat=`date`

echo $date

echo "the date is ${date}"

```

## Argument Pass

1) argument variable *
2) getopts f(n)

## Special Shell Variables

| Variable  | Description                                            |
|-----------|--------------------------------------------------------|
| `$1-$9`   | Positional arguments for the script (up to $9).        |
| `$10-$n`  | Positional arguments beyond $9 (e.g., `$10`, `$11`, etc.). |
| `$0`      | Name of the script or command.                         |
| `$#`      | Total number of arguments passed to the script.        |
| `$$`      | Process ID (PID) of the currently executing script.    |
| `$HOSTNAME` | The hostname of the machine running the script.       |
| `$USER`   | The username of the current user.                      |
| `$RANDOM` | Generates a random number between 0 and 32767.         |


## Give Input

Take input at the run time of the programm.
```
echo "hello there, Enter your name"
read <your variable name>
read ans
echo "Your name is $ans"
```
## To print multiple value
```
#!/bin/bash
read -p "enter the number:" n1         # -p for prompt
read -p "enter the number:" n2
read -p "enter the number:" n3
#display three no.
echo "Number1 - $n1"
echo "Number1 - $n1"
echo "Number1 - $n1"
```

## Display the domain name
```
read -t 2 -p "enter the domain name:" domain_name
whois $domain_name
```
 `-t` for time to leave or automatic fill input and process it
```
read -s -p "enter password:" passwd     #-s for silent
echo "your password: $passwd"
```


## Conditional statement

1. if statements
2. if else statement
3. if elif statement
4. nested if statement
5. case(switch) statement

## Condition Operators

| Operator | Description                                      |
|----------|--------------------------------------------------|
| `-eq`    | Equal (`=`)                                      |
| `-lt`    | Less than (`<`)                                  |
| `-le`    | Less than or equal to (`<=`)                     |
| `-gt`    | Greater than (`>`)                               |
| `-ge`    | Greater than or equal to (`>=`)                  |
| `==`     | Equal                                            |
| `!=`     | Not equal                                        |
| `!`      | Not                                              |
| `-d`     | Check if directory exists                        |
| `-e`     | Check if file exists                             |
| `-r`     | Check if file is readable                        |
| `-w`     | Check if file is writable                        |
| `-x`     | Check if file is executable                      |

## Syntax
```
if [condition]; then
echo "statement"
fi
```
## Example 1.:
```
read -p "what is your age:" age
if [$age -lt 18]; then
ehco "you are no eligible for voting"
fi
```
## Example 2.:
```
#!/bin/bash
#if another example

echo "enter any number:"
read n
if [ $n -gt 100]; then
echo "$n is greater than 100\n"
fi
```

























