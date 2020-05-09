# Competitive coding environment setup

Bash script starter project to automate setting up of a local testing environment for competitive coding. This only works on unix systems or subsystems which run bash. The library currently supports c++, c and python.

## Requirements

In order to work with the current library, you will need the following requirements

1. A system which can run bash script, a unix system.
2. In order to work with the required language you will need the language's native dependencies to be installed, for python you will need python 3 installed, for c++ and c you will need g++ and gcc respectively.

## Setup

First clone the repository and keep it in a location you will not change the file from, for instance you may clone it into your ~/ repository.

### Adding to path (optional)

To make the program easy to use, we can add the file to the system path.

In order to so we first edit the following file

```bash
nano ~/.bash_profile
```

We then add the following line,

```bash
export PATH=$PATH:<BASE_PATH>/ccautomate/bin
```

Upon doing so, run the following to finalize the changes

```bash
source ~/.bash_profile
```

And restart your terminal.

### Permissions

We have to give execute permissions to the ccautomate.sh file.

```bash
$ chmod +x <BASE_PATH>/ccautomate
```

## Using the library

Now, open the directory you wish to setup your environment in and run the following

```bash
$ ccautomate <language>
```

where language is the language you want to setup the environment for, the following languages are supported

1. python3
2. c++
3. c

## Environment

The environment will consist of three files

1. 1.in - the file containing the stdin/input to the program
2. sol - this file is where you write the solution for your required problem
3. run.sh - this is the bash file you run in order to test out your solution

   ```bash
   $ ./run.sh
   ```

The stdout will be displayed in the terminal you ran your program from.
