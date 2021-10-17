# Clean install options for Windows 10

## Windows 10 Professional
I begin with a fresh clean install of Windows 10 Professional. Somday I will document the settings I go though but
for now I just do the basic. 

* Language: English
* Keyboard: US inernational
* Disable most of the diagnositics questions
* Use my AzureAd account to signin

Then first I install my [default software set](software.md) and then go though some setup.

* Setup Onedrive for Business
* Setup some Shareoint folders I like to keep available
* Start the Windows Mail App (I don't use Outlook) and make sure my email is there
* Start Word for the first time, assign my account and choose the Microsoft docx format

I like to have my files in the root of C:\data or on a D:\ drive depending on what the computer has.
* Create a c:\data folder

```
app
    <folders for portable / xcopy apps >
data
    git
    dev
    nuget
    vsts
    temp
```
* git is the default location to put github repo's. I keep my git DevOps repo's under vsts
* dev a folder for some local test development not under sourcecontrol
* nuget a folder for my local nuget cache. I configure a .nuget file in a root per dev folder or solution so all nuget packages are downloaded here. I know, but I like to prevent massive amounts of duplicate files
* vsts my DevOps sourcecontrolled files. The name should change but since MS changes product names soo fast I am sticking with this for now. Previously I would use "visualstudioonline" :-|
* temp is as the names suggests for temp files, I don't like c:\windows\temp and have resisted c:\temp
* iso is a folder I sometimes have to store .iso files that I keep longer. Usually the end up in temp of stay in the system Downloads folder
* vhd or Hyper-V if I have that anabled and use it.
* wsl is a place to store wsl specific stuff


After having setup my folders I can continue setting up software

## Visualstudio 2019
* Start Visualstudio and configure that to use c:\data\dev as default folder for new solutions

## Visualstudio Code
Some usefull extensions I tend to install everytime

* Live Server (ritwickdey.liveserver)
* Azure Account (ms-vscode.azure-account)
* C# (ms-dotnettools.csharp)
* Paste JSON as Code (quicktype.quicktype)
* Remote WSL (ms-vscode-remote.remote-wsl)
* Git Graph (mhutchie.git-graph)
* Bracket Pair Colorizer 2 (coenraads.bracket-pair-colorizer-2)

* Bootstrap 4, Font awesome 4, Font Awesome 5 Free & Pro snippets (thekalinga.bootstrap4-vscode)
* Angular 8 Snippets - TypeScript, Html, Angular Material, ngRx, RxJS & Flex Layout (Mikael.Angular-BeastCode)

## Edge
I use a few extensions in the browser.

* Lastpass
* Json Beautifier and editor

## Regedit hacks
Some settings are not simply available and we have to resort to registry hacks. I hate some of the default folders Windows displays so I clean them up.

[Remove Music and Videos folders](./Settings/registry/regedit-hide-music-and-videos-from-this-pc.reg)