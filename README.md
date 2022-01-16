# Windows Teminal Customization

## These tweaks / custimizations techniques are Windows Only

Very often I'm asked how I customized my Windows Terminal. This repo will walk you through step-by-step how to make your terminal look like the one I use.
Fisrt of all, let's have look at my Windows Terminal.

### Desclaimer: Windows Powershell (legacy version) support will be dropped soon. It's better to go with PowerShell Core

### Let's take look at the final result we are trying to achive

![preview](https://github.com/evilprince2009/Windows-Terminal-Customization/blob/main/images/preview.gif)

Now, let's start customizing the terminal. First things first , let's go through the prerequisites.

### Prerequisites

- Windows PowerShell or PowerShell Core
- [Windows Terminal](https://www.microsoft.com/en-us/p/windows-terminal/9n0dx20hk701#activetab=pivot:overviewtab)
- [CascadiaCode](https://github.com/ryanoasis/nerd-fonts/releases/download/v2.1.0/CascadiaCode.zip)
- Dependencies
- [Git](https://git-scm.com/downloads)
- [DotFetch](https://github.com/evilprince2009/DotFetch) or [DotFetch.NET](https://github.com/evilprince2009/DotFetch.NET) (Recommended: DotFetch)

## How to's

### Windows PowerShell or PowerShell Core

Windows PowerShell legacy version comes built in with Windows. You can download the latest version of PowerShell Core from _[here](https://github.com/PowerShell/PowerShell/releases)_. I strongly recommend using PowerShell Core.

### Install Windows Terminal

Definitely if you haven't installed Windows Terminal yet, install it from Microsoft Store. Thats the must thing you need to do.

### Install CascadiaCode

Download the [CascadiaCode](https://github.com/ryanoasis/nerd-fonts/releases/download/v2.1.0/CascadiaCode.zip) font latest version and install it on your computer. This should be very straight forward. Using other fonts might create gibberish on the terminal and break the design , probably you won't get all those nice glyphs.

### Install Dependencies

If you want to have colorful themes in your terminal, you need to install some dependencies. Install these dependencies listed below.

Install below dependencies.

- If you don't have _Winget_ or _Chocolatey_ installed on your system , get them. Now run `winget install JanDeDobbeleer.OhMyPosh` or `choco install oh-my-posh` from terminal and wait for the OMP V3 installation to complete.

- Install `PSReadLine` from _[here](https://www.powershellgallery.com/packages/PSReadLine/2.2.0-beta1)_
- Install `Terminal-Icons` from _[here](https://www.powershellgallery.com/packages/Terminal-Icons/)_
- Install `z` from _[here](https://www.powershellgallery.com/packages/z/1.1.13)_

Using the latest version of dependencies is strongly recommended. With Windows PowerShell (legacy version) Sometimes, you might get some error while installing those modules. In that case, you can install them manually. Those modules are usually located in `C:\Program Files\WindowsPowerShell\Modules`.

### Install Git

Download the [Git for Windows](https://gitforwindows.org/downloads) and install and configure it on your system properly. You can check out this [video](https://www.youtube.com/watch?v=8JJ101D3knE&t=762s) to see how to install and configure Git properly on Windows.

### Workspace directory

Make a folder named `Workspace` in your `D:\` Drive.

### Install DotFetch or DotFetch.NET

Head over to [DotFetch](https://github.com/evilprince2009/DotFetch) or [DotFetch.NET](https://github.com/evilprince2009/DotFetch.NET) repo and go through the README , and follow the instructions to install it properly on your system. I recommend using [DotFetch](https://github.com/evilprince2009/DotFetch) for the instructions I wrote here.

### Update PowerShell profile

After opening profile by `notepad $profile` on terminal and Enter , open this **[PSCore_profile.ps1](https://github.com/evilprince2009/Windows-Terminal-Customization/blob/main/PSCore_profile.ps1)** file , copy everything and paste in your PowerShell profile. This is the configuration I recommend. You will get intellisense , auto-completion , nice keybindings like `Ctrl+Shift+B` for running commands like `dotnet build` from terminal and much more. Below animated gif is a sneak peak actually what you are going to have.

![terminal-intellisense](https://github.com/evilprince2009/Windows-Terminal-Customization/blob/main/images/terminal-intellisense.gif)

_Auto-Completion , Intellisense in Terminal._

This kind of Auto-Completion , Intellisense is can smoothly be implemented for PowerShell Core. This feature also works with Windows PowerShell , but you have to download and configure `PSReadLine` module latest version properly since it has some compatibility issues with Windows PowerShell (legacy version).

### Write your custom settings

- Hit `Windows+R` to open the run command.
- Paste `%USERPROFILE%\AppData\Local\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState` and hit enter. This will bring up a file explorer.
- Now download the `settings.json` file from _[here](https://github.com/evilprince2009/Windows-Terminal-Customization/blob/main/settings.json)_ and paste it in the file explorer.

### Customize themes and color scheme even more

- To see the list of available themes , run `Get-PoshThemes` on terminal.
- To customize color scheme of your favourite theme , navigate to `%USERPROFILE%\AppData\Local\Programs\oh-my-posh\themes` directory for OMP v3.

- Open the theme file you want to customize in your preferred code editor and modify the color scheme. Make sure to save the changes you made.

### Tip

Those who wants to customize the default color scheme of posh themes , might be interested to have look at how it is done. I've modified two of them & here it is.

- Check out modified _iterm2_ theme (`iterm2.omp.json`) file _**[here](https://github.com/evilprince2009/Windows-Terminal-Customization/blob/main/modified_posh_themes/iterm2.omp.json)**_.

- Check out modified _powerlevel10k-rainbow_ theme (`powerlevel10k_rainbow.omp.json`) file **[here](https://github.com/evilprince2009/Windows-Terminal-Customization/blob/main/modified_posh_themes/powerlevel10k_rainbow.omp.json)**.

### Now it's showtime

Once you are done , re-launch your Windows Terminal and you should be good to go.

### Note: As I maintain and update this repository on a regular basis , scripts and dependencies gets changed frequently. You are requested to follow the instructions and use confugurations from main repository. If you follow any fork of this repo which has been modified by someone else and you break something , I'm not responsible

### [Ibne Nahian](www.facebook.com/evilprince2009)
