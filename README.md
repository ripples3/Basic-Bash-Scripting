# Learning Basic Bash Scripting

## License

The guide may be used and shared for educational, non-commercial, not-for-profit purposes. Users are free to modify and distribute content.

### Let's create a simple scirpt

1. We will create a file, first.sh (you can use any text editor)
2. The first line will be **#! /bin/sh** (it tells the interpreter that it is a bash script).
3. We will write a command ls(list the subfolders in the directory)

```
#! /bin/sh
ls
```
4. Run the script by executing command **./first.sh**

Suppose, you have to push a commit to your git repository. Instead of writing the commands one by one, we can write a shell script that automates the whole process. Create a file git.sh

```
#! /bin/sh 
git add .
git commit -m $1
git push origin master
```
We will automate the process of pushing commit to the repo. $1 is a variable that will get the input that the user will provide.
To run this script, execute ./git.sh ‘initial commit’. ‘initial commit’ will be placed at the $1.


### Comments
Comments in shell scripts are followed by #.
```
# This is a comment.
```

### Variables
Variables are declared using the =
```
MY_NAME='Morty' #No spaces 
```
```
NAME="John"
echo $NAME
echo "$NAME"
echo "${NAME}!"
```
Variables are accessed using the $ sign.

### String
String are assigned to a variable
```
NAME="John"
echo "Hi $NAME"  #=> Hi John
echo 'Hi $NAME'  #=> Hi $NAME
```


### Echo
Echo is used to display the statement in the shell just like printf in C language.
```
MY_NAME='Morty' 
echo "My name is $MY_NAME"

<Output>
# My name is Morty
```

### Conditional Statements
Let’s see how an if else statement looks in bash scripting.
```
if [[condition]];
then
# write the then instructions here
else
# write the else instructions here
fi
```
```
if [[ -z "$string" ]]; then
  echo "String is empty"
elif [[ -n "$string" ]]; then
  echo "String is not empty"
fi

```
### Conditional execution
These are some of conditions
```
git commit && git push
git commit || echo "Commit failed"
```

### Functions
Functions are group of statements that together perform a task.
```
get_name() {
  echo "John"
}
echo "You are $(get_name)"
```

### Loops
#### Basic for loop
```
for i in /etc/rc.*; do
  echo $i
done
```
