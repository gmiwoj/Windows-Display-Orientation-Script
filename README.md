## windows-screen-rotate-script.ps1

Windows Powershell / .NET script

Flip screen rotation horizontal / vertical quick and easy. Create shortcut to rotate screen 90 degrees quick and easy. Works with dual screen or multiple monitors, rotates both ways. 

Because switching between vertical and horizontal using Display settings on windows takes too many clicks.




![preview2](https://support.content.office.net/en-us/media/96e92630-bbfe-4292-bbfc-fbb4a4908c8e.png)
![preview2](https://www.tenforums.com/attachments/tutorials/268002d1582491524-how-change-display-orientation-windows-10-a-display_orientation.png)





**usage examples (as command or as shortcut):**

switch second screen to vertical inverted:

`powershell.exe -ExecutionPolicy Bypass -File "C:\PATH_TO_SCRIPT\windows-screen-rotate-script.ps1" 1 90`

back to horizontal:

`powershell.exe -ExecutionPolicy Bypass -File "C:\PATH_TO_SCRIPT\windows-screen-rotate-script.ps1" 1 0`



**needs 2 arguments!**
- argument 1 : display id (0 - first main screen, 1 - second screen, 2 - third etc.)
- argument 2 : rotation angle (0 - normal, 90 - vertical clockwise, 180 - upside down, 270 - vertical counter clockwise. can only rotate by 90 in one go, cant go from 0 straight to 180)

so
`... "windows-screen-rotate-script.ps1" 1 90` means second display 90 degrees CW




**disclaimer:**

i didn't write 90% this code myself, i barely know how it works. i just mashed various pieces of code that worked for me, that i found here and there, and modified some parts to my needs.
