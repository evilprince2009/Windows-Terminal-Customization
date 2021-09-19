## Windows Teminal Customization

### These tweaks / custimizations techniques are Windows Only

Very often I'm asked how I customized my Windows Terminal. This repo will walk you through step-by-step how to make your terminal look like the one I use.
Fisrt of all, let's have look at my Windows Terminal.

### Fullscreen Maximized

![terminal](<https://github.com/evilprince2009/Windows-Terminal-Customization/blob/main/images/Screenshot%20(55).png>)

### Resized View

![terminal](<https://github.com/evilprince2009/Windows-Terminal-Customization/blob/main/images/Screenshot%20(57).png>)

Now, let's start customizing the terminal. First things first , let's go through the prerequisites.

### Prerequisites

- [Windows Terminal](https://www.microsoft.com/en-us/p/windows-terminal/9n0dx20hk701#activetab=pivot:overviewtab)
- [Cascadia Code](https://github.com/microsoft/cascadia-code/releases/tag/v2106.17)
- Dependencies
- [Git](https://git-scm.com/downloads)
- [DotFetch](https://github.com/evilprince2009/DotFetch)

## How to's

### Install Windows Terminal

Definitely if you haven't installed Windows Terminal yet, install it from Microsoft Store. Thats the first thing you need to do.

### Install Cascadia Code

Download the [Cascadia Code](https://github.com/microsoft/cascadia-code/releases/tag/v2106.17) font latest version and install it on your computer. This should be very straight forward. Using other fonts might create gibberish on the terminal and break the design.

### Install Dependencies

If you want to have colorful themes in your terminal, you need to install some dependencies. Install `posh-git` from _[here](https://www.powershellgallery.com/packages/posh-git/)_ and `oh-my-posh` from _[here](https://www.powershellgallery.com/packages/oh-my-posh/)_. You are allowed to use any version of these dependencies. But using the latest version is a recommended.

### Install Git

Download the [Git for Windows](https://gitforwindows.org/downloads) and install and configure it on your system properly. You can check out this [video](https://www.youtube.com/watch?v=8JJ101D3knE&t=762s) to see how to install and configure Git properly on Windows.

### Install DotFetch

Head over to [DotFetch](https://github.com/evilprince2009/DotFetch) repo and go through the README , and follow the instructions to install it properly on your system.

### Update PowerShell profile

Open PowerShell & type `notepad $profile` and hit Enter. This will open a text file in Notepad. Put below lines inside the file and save.

```
Import-Module posh-git
Import-Module oh-my-posh
Set-PoshPrompt -Theme Iterm2
Write-Host("                        =========> Wellcome || Windows PowerShell <=========")
dotfetch
```

### Workspace directory

Make a folder named `Workspace` in your `D:\` Drive.

### Write your custom settings

- Hit `Windows+R` to open the run command.
- Paste `%USERPROFILE%\AppData\Local\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState` and hit enter. This will bring up a file explorer.
- Now download the `settings.json` file from _[here](https://github.com/evilprince2009/Windows-Terminal-Customization/blob/main/settings.json)_ and paste it in the file explorer.

### Customize themes and color scheme even more

- To see the list of available themes , run `Get-PoshThemes` on terminal.
- To customize color scheme of your favourite theme , navigate to `C:\Program Files\WindowsPowerShell\Modules\oh-my-posh\themes` , open the theme file you want to customize in your preferred code editor and modify the color scheme. Make sure to save the changes you made.

### Now it's showtime

Once you are done , re-launch your Windows Terminal and you should be good to go.

### [Ibne Nahian](www.facebook.com/evilprince2009)
