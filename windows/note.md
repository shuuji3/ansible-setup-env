# How to setup Windows

[Install Chocolatey](https://chocolatey.org/install) by running the following command in powershell as the admin.

```shell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

Then, install other software packages:

```shell
choco feature enable -n allowGlobalConfirmation
choco install virtualbox googlejapaneseinput wsl2 scansnapmanager googledrive googlechrome barrier vscode
```
