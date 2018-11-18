# Windows Setup

## Package Manager

[Chocolatey](https://chocolatey.org): "The sane way to manage software on Windows"

We will be installing most of the tools in this guide using CLI via Chocolatey's packages, they understand versioning and dependencies.

Open `cmd` as administrator and type the following command to install Chocolatey:

```
@"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command "iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"
```

For other options and troubleshooting try [this](https://chocolatey.org/install) and you can explore all the packages available with Chocolatey [here](https://chocolatey.org/packages)

## Terminal, shell and modules

We will be installing these set of tools that makes Windows bearable/usable:

* [**cmder**](http://cmder.net/): "a software package created out of pure frustration over the absence of nice console emulators on Windows. It is based on amazing software, and spiced up with the Monokai color scheme and a custom prompt layout, looking sexy from the start."

To make things faster we can start with **cmder mini**(~8.5MB), to install it with Chocolatey, type `choco install cmdermini` or simply `cinst cmdermini`.

You can also install the full version of cmder with `cinst cmder`.

* [**Gow**](https://github.com/bmatzelle/gow): "The lightweight alternative to Cygwin"

Gow (Gnu On Windows) is the lightweight alternative(~10MB) to Cygwin, it installs over 100 extremely useful open source UNIX applications. After instaling Gow, in addition to windows commands you will be able to also run Unix commands like: ls, rm, etc.

To install Gow, type `cinst gow` and press enter.

* [**posh-git**](https://github.com/dahlbyk/posh-git): "A PowerShell environment for Git"

posh-git is a PowerShell module that integrates Git and PowerShell by providing Git status summary information that can be displayed in the PowerShell prompt, posh-git also provides tab completion support for common git commands, branch names, paths and more.

To install posh-git, type `cinst poshgit` and hit enter.

#### powershell profile

run notepad $profile.CurrentUserAllHosts to edit it.
  
    Import-Module posh-git in the file
    New-Alias ll Get-ChildItem

The above will
* import posh-git module
* create an alias of "ll", to do "dir"


### Node

```
cinst nodejs.install

npm install -g npm-windows-upgrade
npm-windows-upgrade
```

### Version Control

on windows
```
cinst git.install
cinst poshgit

# Restart PowerShell / CMDer before moving on - or run
$env:Path = [System.Environment]::GetEnvironmentVariable("Path","Machine") + ";" + [System.Environment]::GetEnvironmentVariable("Path","User")

cinst Git-Credential-Manager-for-Windows
cinst github
```

### Editors: VS Code

```
cinst visualstudiocode
cinst visualstudio2017community
```

### Ruby
Even if you don't care about Ruby at all, bear in mind that it's preinstalled on OS X (and easy to install on Unix), so many dev tools might be trying to leverage it. For example, GitHub pages are compiled using Jekyll - if you want to get in on that, install Ruby.

```
cinst ruby
cinst ruby.devkit
```

#### Azure Cli
Super duper useful if you're working with Azure at all.
```
npm install -g azure-cli
```

#### AWS Cli
Super duper useful if you're working with Amazon Web Services at all.
```
cinst awscli
cinst awstools.powershell
```

### Basic Tools
You'll recognize many of these names. Nothing here is crazy unique, it's just stuff you probably want installed to have a well-running machine.

```
cinst vlc
cinst GoogleChrome
cinst 7zip.install
cinst sysinternals
cinst DotNet3.5
```

If you're not running Windows 10, also install:

```
cinst DotNet4.0 -- not needed on windows 8
cinst DotNet4.5 -- not needed on windows 10
cinst PowerShell -- not needed on windows 10
```
