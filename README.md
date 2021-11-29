## windows-screen-rotate-script.ps1

Windows Powershell / .NET script

Flip screen orientation horizontal / vertical quick and easy with a command or shortcut icon. Because switching between landscape and portrait mode using Display settings on windows takes too many clicks.

Works with multiple monitors and all display orientation modes (landscape, landscape inverted, portrait, portrait inverted).


[Download script](https://raw.githubusercontent.com/gmiwoj/windows-screen-rotate-script.ps1/main/windows-screen-rotate-script.ps1) <-- right click, Save as



![preview2](https://support.content.office.net/en-us/media/96e92630-bbfe-4292-bbfc-fbb4a4908c8e.png)



### usage examples (as commands or as shortcuts) :

switch second screen to portrait (vertical counter clockwise) :

`powershell.exe -ExecutionPolicy Bypass -File "C:\PATH\windows-screen-rotate-script.ps1" 1 270`

switch second screen to portrait inverted (vertical clockwise) :

`powershell.exe -ExecutionPolicy Bypass -File "C:\PATH\windows-screen-rotate-script.ps1" 1 90`

switch second screen back to landscape (horizontal) :

`powershell.exe -ExecutionPolicy Bypass -File "C:\PATH\windows-screen-rotate-script.ps1" 1 0`



### needs 2 arguments! :
- argument 1 : display id (0: first main screen, 1: second screen, 2: third etc.)
- argument 2 : rotation degree (0: default landscape, 90: portrait inverted, 180: landscape inverted, 270: portrait. 

so :

- `... windows-screen-rotate-script.ps1" 0 270` means first primary display, 90 degrees ccw (vertical)
- `... windows-screen-rotate-script.ps1" 1 90`  means second display, 90 degrees cw (vertical inverted)


can only rotate by 90 in one go for some reason, can't go from 0 straight to 180, needs 2 steps).

can't set screen xy position in relation to other screens as possible with Display settings menu. 



### disclaimer :

i didn't write 90% this code myself, i barely know how most of it works. i just mashed various pieces of code that worked for me found on the internet and modified some parts to my needs. sharing it now with anyone that might find it useful.
