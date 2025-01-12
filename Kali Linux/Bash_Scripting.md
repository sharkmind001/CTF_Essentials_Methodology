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

## Example 3.: (example of if, elif ,else)
```
read -p "enter the marks:" marks

if (( $marks >= 90 )); then
echo "Grade is A+"
elif (( $marks < 90 && $marks >= 80 )); then
echo "Grade is A"
elif (( $marks < 80 && $marks >= 70 )); then
echo "Grade is B+"
elif (( $marks < 70 && $marks >= 60 )); then
echo "Grade is C"
else
echo "Grade is F"
fi
```
## Swicth
```
#!/bin/bash
#case statment

echo "which color you like"
echo "1 - blue"
echo "2 - red"
echo "3 - yellow"
echo "4 - green"
echo "5 - orange"
read color

case $color in 
1) echo "blue is a primary color.";;
2) echo "red is a primary color.";;
3) echo "yellow is a primary color.";;
4) echo "green is a primary color.";;
5) echo "orange is a primary color.";;
*) echo "This is not available. Please the different color.";;
esac
```


## Function
```
func_name(){statment}      #defining the function

func_name(){
  statment
}

func_name                  #calling a function
```
## Another way
```
function func_name{
  statment
}
```

## Example 1.:
```
function func_name{
echo "this is function"
}

func_name
```
```
Output: this is function

```


## Local and Globle scope

By default all variable is globle still fuction variable

### Example.:
```
var1=a
var2=b

my_var() {
local var1=c
local var2=d

echo "inside function"
echo "var1 is $var1"
echo "var2 is $var2:
}

echo "before executing the function"
echo "var1 is $var1"
echo "var2 is $var2"
 
my_var

echo "after executing the function"
echo " var1 is $var1"
echo "var2 is $var2"
```
### Example 2.: Returning value
```
add() {
result=$(($1 + $2))
}

add 14 5
echo "the sum is : $result"
```
```
Output: the sum is : 19

```

## Loops

### For loop

**Example 1.:**
```
echo "list partitions under the disk"
for i in /dev/sda*; do
echo "$i"
done
```
**Example 2.:**
```
for i in {1..5}; do echo "number: $i"; done            // ";" used to break line
```
Example 3.:
```
for ((i=1; i<=5 i++)) do echo "number: $i"; done 
```


**Example 4.: wap to print even number**
```
for i in {1..10};
do 
if [ $((i%2)) -eq 0 ];
then 
echo "$i even"
fi
done
```
## While loop:
```
read -p "Enter the number to print the table:" num 
i=1
while [ $i -le 10 ]
do 
echo "$num x $i = $((num*i))"
i=$((i+1))  
done
```
## Until loop:
The block of statment are executed until the expression return the true.
```
until [ expression ]; do
	statment(5)
done
```


**Example.:**
```
count=10
i=20

until [$i -lt $count ]; do
echo "$i"
((i--))
done
```
## Array

**Syntax.:**
```
color=("Blue" "Black" "Brown"); echo ${color[@]}

color=([1]="Blue" [2]="Black" [3]="Brown"); echo ${color[@]}

color=([1]="Blue" [2]="Black" [3]="Brown"); echo ${color[2]}; echo ${color[3]}
```
## Find array length
```
color=("Blue" "Black" "Brown"); len=${#color[@]}; echo "Length of array : $len"
```

**'#' for find length of the  array**

### Access element of array using index
```
color=("black" "blue" "brown"); echo ${color[0]} 

color=("black" "blue" "brown"); echo ${color[*]};      #for all the elements

color=("black" "blue" "brown"); echo ${color[@]};      #for all the elements

color=("black" "blue" "brown"); echo ${color[0]}; echo ${color[2]};
```
## Bash Read File
```
var=`cat read.txt`; echo $var

var=$(<read.txt); echo $var
```
## Bash Date & Time
```
dt=$(date); echo $dt

dt=`date +%m-%d-%Y; echo $dt          #In mm-dd-yyyy format
```

## Time Format Specifiers

| Format | Description                             |
|--------|-----------------------------------------|
| `M`    | Minutes                                 |
| `m`    | Month (numeric value, e.g., `04` for April) |
| `B`    | Full month name (e.g., `April`)         |
| `b`    | Short month name (e.g., `Apr`)          |
| `A`    | Full weekday name (e.g., `Monday`)      |
| `a`    | Short weekday name (e.g., `Mon`)        |


## Time
```
hr=$(date +%H); echo "$hr"  
```

| Format | Description                             |
|--------|-----------------------------------------|
| `H`    | 24-hour format (e.g., `14` for 2 PM)    |
| `I`    | 12-hour format (e.g., `02` for 2 PM)    |

```
echo Hours = $(date +%H)
echo Minutes = $(date +%M)
echo Seconds = $date +%S)
echo Nanosecond = $(date +%N)

echo "current time = $(date +%H:%M:%S:%N)"
echo "current time in 24 hour = $(date +%T)"
echo "current time in 12 hour = $(date +%r)" 

```

## Bash Sleep

Bash sleep command is used to insert a delay or pause the execution  for a specific period of time.

**Syntax.:**

`sleep no.[suffix]`
```
sleep 3[s-second]
	[m-minute]
	[h-hour]

echo HH:MM:SS
echo `date +%H:+%M:+%S/%m-%d-%Y`;
sleep 4
echo `date +%H:+%M:+%S/%m-%d-%Y`;

```
## Colorfull text
```
red="\033[31m"
green="\033[0;32m"
yellow="\033[0;33m"
no_color="\033[0m"
```


30-37 sets foreground color

40-47 sets background color

## Color Codes

| Color        | Code      | Description         |
|--------------|-----------|---------------------|
| Black        | 30        |                     |
| Red          | 31        |                     |
| Green        | 32        |                     |
| Yellow       | 33        |                     |
| Blue         | 34        |                     |
| Purple       | 35        |                     |
| Cyan         | 36        |                     |
| White        | 37        |                     |

## Reset

| Color        | Code      | Description         |
|--------------|-----------|---------------------|
| Reset        | `\033[0m` | Text Reset          |

## Regular Colors

| Color        | Code      | Description         |
|--------------|-----------|---------------------|
| Black        | `\033[0;30m` | Regular Black     |
| Red          | `\033[0;31m` | Regular Red       |
| Green        | `\033[0;32m` | Regular Green     |
| Yellow       | `\033[0;33m` | Regular Yellow    |
| Blue         | `\033[0;34m` | Regular Blue      |
| Purple       | `\033[0;35m` | Regular Purple    |
| Cyan         | `\033[0;36m` | Regular Cyan      |
| White        | `\033[0;37m` | Regular White     |

## Bold

| Color        | Code      | Description         |
|--------------|-----------|---------------------|
| Black        | `\033[1;30m` | Bold Black        |
| Red          | `\033[1;31m` | Bold Red          |
| Green        | `\033[1;32m` | Bold Green        |
| Yellow       | `\033[1;33m` | Bold Yellow       |
| Blue         | `\033[1;34m` | Bold Blue         |
| Purple       | `\033[1;35m` | Bold Purple       |
| Cyan         | `\033[1;36m` | Bold Cyan         |
| White        | `\033[1;37m` | Bold White        |

## Underline

| Color        | Code      | Description         |
|--------------|-----------|---------------------|
| Black        | `\033[4;30m` | Underline Black    |
| Red          | `\033[4;31m` | Underline Red      |
| Green        | `\033[4;32m` | Underline Green    |
| Yellow       | `\033[4;33m` | Underline Yellow   |
| Blue         | `\033[4;34m` | Underline Blue     |
| Purple       | `\033[4;35m` | Underline Purple   |
| Cyan         | `\033[4;36m` | Underline Cyan     |
| White        | `\033[4;37m` | Underline White    |

## Background Colors

| Color        | Code      | Description         |
|--------------|-----------|---------------------|
| Black        | `\033[40m`  | Background Black   |
| Red          | `\033[41m`  | Background Red     |
| Green        | `\033[42m`  | Background Green   |
| Yellow       | `\033[43m`  | Background Yellow  |
| Blue         | `\033[44m`  | Background Blue    |
| Purple       | `\033[45m`  | Background Purple  |
| Cyan         | `\033[46m`  | Background Cyan    |
| White        | `\033[47m`  | Background White   |

## High Intensity

| Color        | Code      | Description         |
|--------------|-----------|---------------------|
| Black        | `\033[0;90m`  | High Intensity Black |
| Red          | `\033[0;91m`  | High Intensity Red   |
| Green        | `\033[0;92m`  | High Intensity Green |
| Yellow       | `\033[0;93m`  | High Intensity Yellow|
| Blue         | `\033[0;94m`  | High Intensity Blue  |
| Purple       | `\033[0;95m`  | High Intensity Purple|
| Cyan         | `\033[0;96m`  | High Intensity Cyan  |
| White        | `\033[0;97m`  | High Intensity White |

## Bold High Intensity

| Color        | Code      | Description              |
|--------------|-----------|--------------------------|
| Black        | `\033[1;90m`  | Bold High Intensity Black |
| Red          | `\033[1;91m`  | Bold High Intensity Red   |
| Green        | `\033[1;92m`  | Bold High Intensity Green |
| Yellow       | `\033[1;93m`  | Bold High Intensity Yellow|
| Blue         | `\033[1;94m`  | Bold High Intensity Blue  |
| Purple       | `\033[1;95m`  | Bold High Intensity Purple|
| Cyan         | `\033[1;96m`  | Bold High Intensity Cyan  |
| White        | `\033[1;97m`  | Bold High Intensity White |

## High Intensity Backgrounds

| Color        | Code      | Description                  |
|--------------|-----------|------------------------------|
| Black        | `\033[0;100m` | High Intensity Background Black |
| Red          | `\033[0;101m` | High Intensity Background Red   |
| Green        | `\033[0;102m` | High Intensity Background Green |
| Yellow       | `\033[0;103m` | High Intensity Background Yellow|
| Blue         | `\033[0;104m` | High Intensity Background Blue  |
| Purple       | `\033[0;105m` | High Intensity Background Purple|
| Cyan         | `\033[0;106m` | High Intensity Background Cyan  |
| White        | `\033[0;107m` | High Intensity Background White |


## 1. color-mode

It modifies the style of color NOT text. For example make the color bright or darker.
```
0; reset
1; lighter than normal
2; darker than normal
```
This mode is not supported widely. It is fully support on Gnome-Terminal.

## 2. text-mode

This mode is for modifying the style of text NOT color.
```
3; italic
4; underline
5; blinking (slow)
6; blinking (fast)
7; reverse
8; hide
9; cross-out
```
The escape character in bash, hex and octal respectively:

## Escape Sequences for Bash Colors

|      | Bash   | Hex        | Octal    | Notes                                     |
|------|--------|------------|----------|-------------------------------------------|
| Start | `\e`    | `\x1b`     | `\033`   | Commonly used to begin escape sequences    |
| Start | `\E`    | `\x1B`     | -        | Note: `x` cannot be capitalized           |
| End   | `\e[0m` | `\x1b[0m`  | `\033[0m`| Resets all attributes to defaults         |
| End   | `\e[m`  | `\x1b[m`   | `\033[m` | `0` is appended automatically if omitted  |

**Ex.1.:**
```
RED='\033[0;31m'
NC='\033[0m' # No Color
Green='\033[0;32m'
printf "I ${RED}love${Green} Stack Overflow\n"
```
**Ex.2.:**
```
echo "\033[36m I am Amit"
```
## For terminal styling (nano .zshrc file)
```
PROMPT=$'%F{%(#.blue.green)}┌──${debian_chroot:+($debian_chroot)─}${VIRTUAL_ENV:+($(basename $VIRTUAL_ENV))─}[%B%F{%(#.red.blue)}%n'$prompt_symbol$'%m%b%F{%(#.blue.green)}]-[%f%F{white}%D{192.168.159.148}%f%F{green}]-[%f%F{cyan}%D{vulnos 192.168.159.162}%f%F{green}]-[%B%F{reset}%(6~.%-1~/…/%4~.%5~)%b%F{%(#.blue.green)}]\n└──╼%B%(#.%F{red}#.%F{blue}$)%b%F{reset} '
```





