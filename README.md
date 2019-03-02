# Learning Basic Bash Scripting

## License

The guide may be used and shared for educational, non-commercial, not-for-profit purposes. Users are free to modify and distribute content.

### Let's create a simple scirpt

1. We will create a file, first.sh (you can use any text editor)
2. The first line will be ***#! /bin/sh** (it tells the interpreter that it is a bash script).
3. We will write a command ls(list the subfolders in the directory)

```
#! /bin/sh
ls
```

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
