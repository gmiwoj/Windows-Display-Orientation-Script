## Windows Display Orientation Script

Windows Powershell / .NET script

Instantly flip screen orientation horizontal / vertical with a shortcut icon or command. Because switching between landscape and portrait mode using Display settings on windows takes too many clicks.

Works with multiple monitors and all display orientation modes (landscape, landscape inverted, portrait, portrait inverted).


[Download script](https://raw.githubusercontent.com/gmiwoj/Windows-Display-Orientation-Script/main/windows-display-orientation-script.ps1) <-- right click, Save as



![preview2](https://support.content.office.net/en-us/media/96e92630-bbfe-4292-bbfc-fbb4a4908c8e.png)



### usage examples (as commands or as shortcuts) :

switch second screen to portrait mode (rotate counter clockwise) :

`powershell.exe -ExecutionPolicy Bypass -File "C:\PATH\windows-display-orientation-script.ps1" 1 270`

switch second screen to portrait inverted mode (rotate clockwise) :

`powershell.exe -ExecutionPolicy Bypass -File "C:\PATH\windows-display-orientation-script.ps1" 1 90`

switch second screen back to landscape mode (horizontal) :

`powershell.exe -ExecutionPolicy Bypass -File "C:\PATH\windows-display-orientation-script.ps1" 1 0`

reset all screens to default landscape mode :

`powershell.exe -ExecutionPolicy Bypass -File "C:\PATH\windows-display-orientation-script.ps1"`


### needs 2 arguments! :
- argument 1 : display id (0: first main screen, 1: second screen, 2: third etc.)
- argument 2 : rotation angle (0: default landscape, 90: portrait inverted, 180: landscape inverted, 270: portrait) 

so :

- `... windows-display-orientation-script.ps1" 0 270` means first primary display, 90 degrees ccw to vertical
- `... windows-display-orientation-script.ps1" 1 90`  means second display, 90 degrees cw to vertical inverted

running script without arguments resets all displays to default landscape orientation


### notes :

- doesn't need to be run as admin
- rotation can only be set to 4 available values (0, 90, 180, 270), any other value won't work. 
- can only rotate by 90 degrees in one go for some reason, can't go from 0 straight to 180, needs 2 steps for that.
- can't set screen xy position in relation to other screens as possible with Display settings menu. 
- you can rename script file and keep in any folder, just use full proper path when running it


### disclaimer :

i didn't write 90% of this code myself, i barely know how any of it works. i just mashed various pieces of code i've found on the internet that worked for me and added or modified some parts to my needs. as well as i was able. works as it is, no guarantees. 

sharing it with anyone that might find it useful.
