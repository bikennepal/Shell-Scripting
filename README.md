# Shell-Scripting from Zero to Hero By Turotial point.

Always make a habit of writing an author name in the script
#!/bin/sh

# Author : Zara Ali
# Copyright (c) Tutorialspoint.com
# Script follows here:

echo "What is your name?"
read PERSON
echo "Hello, $PERSON"  
============================

# Read-only Variables

#!/bin/sh

NAME="Zara Ali"
readonly NAME
NAME="Qadiri"
# We cannot change the above variable as this is readonly variable
unset variable_name
Variable & Description: 
$0: the current filename
$n: the positinal paramaters
$#: number of arguments supplied to a script
$*:All the arguments are double quoted. If a script receives two arguments, $* is equivalent to $1 $2.
$@:All the arguments are individually double quoted. If a script receives two arguments, $@ is equivalent to $1 $2.
$?:The exit status of the last command executed.
$$:The process number of the current shell. For shell scripts, this is the process ID under which they are executing.
$!:The process number of the last background command.

# \Special Parameters $* and $@
There are special parameters that allow accessing all the command-line arguments at once. $* and $@ both will act the same unless they are enclosed in double quotes, "".

Both the parameters specify the command-line arguments. However, the "$*" special parameter takes the entire list as one argument with spaces between and the "$@" special parameter takes the entire list and separates it into separate arguments.

We can write the shell script as shown below to process an unknown number of commandline arguments with either the $* or $@ special parameters −


simple shell script to execute the above two special parameters

#!/bin/bash
	for TOKEN in $*
	do
		echo ${TOKEN}
	done
	
================================================================
Arrays in linux:
A variable which hold single value is known as scaler variable: 
A variable which holds multiple items is know as Array:

If you are using the bash shell, here is the syntax of array initialization:
array_name=('biken', 'nepal')
below is how we can access:
${array_name[index]}

To do simple calculation we can use expression:
#!/bin/sh

val=`expr 2 + 2`
echo "Total value : $val"

[ ! flase ] is this true as this is preceeded by ! not in the beginning.
-o is OR in shell and -a is AND in shell script.

==========================================================================
String Operator:

-z -n str and etc learn more.

============================================================================
Sed:

sed 's/sample/are/g'  file.txt

grep, awk and sed.

example: df -h | grep "root"

awk

example: df -h | awk 'NR == 2 { print}'

sed-print:

sed 'p' --> this will print both given line as well as print the line

sed -n '2p' file.txt --> this will print the particular line

sed -d -a -s this willl be for deleting,adding,and subtitute

sed delete:

sed '3','4d' employee.txt

sed -i '3','4d' employee.txt will not print the output in the console

find:

sed search:
'/word-to-serach/'
sed -n '/manager/p' emplyee.txt
sed -n '/\bMa\b/p' employee.txt

sed -n -e '/\bMa\b/p' -e '/\bMa\b/p' employee.txt  we can search in this way if we want two or more.

substutute:
sed 's/sample/are/g'  file.txt

not only substitute but sed command can also insert change and add data in the file.

=====================================================













		




