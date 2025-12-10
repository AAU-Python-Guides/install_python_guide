# Install of Python

Note that you can install python in many ways.

The easiest way to get everything setup as you need to is to use a package manager, for windows I use `choco`, and for macos I would use `brew`.


## MacOS
Homebrew package manager installation guide, see [https://brew.sh/](https://brew.sh/)

Inside terminal:
```bash
brew upgrade
brew cask upgrade
brew cleanup
brew install git
brew install --cask visual-studio-code
brew install python
brew link python@3.14
brew install --cask spyder
python -m ensurepip --default-pip
pip install -r requirements.txt
```

## Windows 10/11
Choco package manager installation guide, see [https://chocolatey.org/install](https://chocolatey.org/install)



Inside terminal:
```bash
choco upgrade all
choco install git
choco install vscode
choco install python314
choco install spyder
python -m ensurepip --default-pip
pip install -r requirements.txt
```

*If Any of the following commands gives an error, write the following in the terminal: "`Set-ExecutionPolicy Unrestricted -Scope LocalMachine`", and run the command again.*

### In Windows you also need to go and disable program aliases.

```zsh
Settings >> Apps >> Advanced App Settings >> App Execution Aliases

Disable:  App Installer assocaited with Python 

App Installer > python.exe > Set to Off
App Installer > python3.exe > set to Off
``` 

![Setup1](alias_disable.png)

## Running Python Instance

inside terminal write:
```bash
python --version
```

This prints the version of python that matches the above you just installed.

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

