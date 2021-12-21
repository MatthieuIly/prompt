
- Install Windows terminal from Windows store
- Install powershell from Windows store
- hide old powershell terminal in settings.json
- Set PowerShell to defaultProfile
- Install Wsl (Ubuntu)
- Windows Terminal : settings.json - Add "commandline": "wsl ~",

#### Fonts
- nerdfonts.com ⇒ fonts download ⇒ Caskaydia Cove nerd font
- Add fonts to C:\Windows\Fonts

#### Install ohmyposh.dev
- Follow Windows\Winget installation
- Windows Terminal : Change PowerShell and Ubuntu appearances to "Caskaydia NF"
    echo $PROFILE
- Create Microsoft.PowerShell_profile.ps1 file and add :
> oh-my-posh --init --shell pwsh --config ~/jandedobbeleer.omp.json | Invoke-Expression

#### Install GutHub.cli

    winget install GitHub.cli --source winget
    gh auth login

#### Ohmyposh
Download [**ohmyposhv3-v2.json**](https://gist.github.com/shanselman/1f69b28bfcc4f7716e49eb5bb34d7b2c?WT.mc_id=-blog-scottha#file-ohmyposhv3-v2-json)

In Microsoft.PowerShell_profile.ps1,  replace jandedobbeleer.omp.json by ohmyposhv3-v2.json
  
#### Install Terminal-Icons

    Install-Module -Name Terminal-Icons -Repository PSGallery
  
add one line in $PROFILE (code $profile)

    Import-Module -Name Terminal-Icons
  
Replace in c:\users\youruser\documents\PowerShell\Microsoft.PowerShell_profile.ps1

#### Install PSReadLine
https://github.com/PowerShell/PSReadLine

    Install-Module -Name PowerShellGet -Force
    Exit

    Install-Module PSReadLine -AllowPrerelease -Force

#### Install z

    Install-Module z -AllowClobber

#### Install oh-my-posh for Linux

Same json file ohmyposhv3-v2.json

#### WSL
If problem Internet connexion
PowerShell

    ipconfig

copy wsl IP

In wsl 

    sudo nano /etc/resolv.conf
    
    nameserver ipwsl


