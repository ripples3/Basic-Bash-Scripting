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
Variables are accessed using the $ sign.


In the above script, we automate the whole process of pushing the commit to the repo. I used $1 in the above code, it is like a placeholder for the input that the user will provide.To run this script, write bash git.sh ‘initial commit’. Here the ‘initial commit’ will be placed at the $1.

Instead of writing the git commands manually, we automate the process by running the script. Let’s take a deep dive into shell scripting.


In the above script, we automate the whole process of pushing the commit to the repo. I used $1 in the above code, it is like a placeholder for the input that the user will provide.To run this script, write bash git.sh ‘initial commit’. Here the ‘initial commit’ will be placed at the $1.

Instead of writing the git commands manually, we automate the process by running the script. Let’s take a deep dive into shell scripting.


### Install the [Documentation Builder](https://github.com/OpenInternet/Documentation-Builder.git)

[Use the installation instructions found here.](https://github.com/OpenInternet/Documentation-Builder/blob/master/docs/INSTALL.md)

### Download the [System Administrator Guide Text](https://github.com/OpenInternet/System_Administrator_Guide_Text)

```
git clone https://github.com/OpenInternet/System_Administrator_Guide_Text.git
```
### Download and Install the [System Administrator Guide Theme Templates](https://github.com/OpenInternet/System_Administrator_Guide_Templates)

```
git clone https://github.com/OpenInternet/System_Administrator_Guide_Templates.git
cd System_Administrator_Guide_Templates
./install
cd ..
```

### Create the System Administrator Guide

```
cd /path/to/documentation/builder/
./builddoc  -i path/to/System_Administrator_Guide_Text/en -t /path/to/System_Administrator_Guide_Templates/ -o output_filename.pdf
```
