# Install of Python

Note that you can install python in many ways.

The easiest way to get everything setup as you need to is to use a package manager, Windows 11 has it's own Package Manager, and for macos I would use `brew`.

## MacOS
Homebrew package manager installation guide, see [https://brew.sh/](https://brew.sh/)

Inside terminal:
```bash
brew upgrade
brew cask upgrade
brew cleanup
brew install git
brew install --cask visual-studio-code
brew install --cask anaconda
```

## Windows 11
You should have the package manager winget on your machines. (Windows 11)



Inside terminal:
```bash
Set-ExecutionPolicy RemoteSigned

winget install anaconda3
winget install MartinStorsjo.LLVM-MinGW.UCRT
winget install Git.Git
winget install vscode
winget install ArduinoSA.IDE.stable

python -m ensurepip --default-pip
pip install -r requirements.txt
```

*If Any of the following commands gives an error, write the following in the terminal: "`Set-ExecutionPolicy Unrestricted -Scope LocalMachine`", and run the command again.*

### In Windows you also need to go and disable program aliases.
if writing `python --version` inside the console, opens the Microsoft Store, do the following:

```zsh
Settings >> Apps >> Advanced App Settings >> App Execution Aliases

Disable:  App Installer assocaited with Python 

App Installer > python.exe > Set to Off
App Installer > python3.exe > set to Off
``` 

![Setup1](alias_disable.png)

## Required Packages
In order to ensure that our python instance has the required packages, we first need to install them into the selected environment.
This can be done using a command like:
```bash
pip install numpy
```
As a convinience, we can use a requirements.txt file, that contains the required python packages.
A `requirements.txt` file example can be seen in this repo.
If we wish to install the packages inside this txt file, we write the following:
```bash 
pip install -r requirements.txt
```

*Note that for virtual environments, the procedure is exactly the same, except we have to have the current environment activated before writing `pip install ...`*

## Git

We might not use Git directly, but it is an extremely powerful tool, that I can only encurage you to investigate further!
New code repositories can be download from terminal using the following command:

```bash
git clone <link>
```

For example

```bash
git clone https://github.com/Anvendt-Programmering/python_serial_recorder.git
```

