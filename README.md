# Preface
This document should be a guide to how set up rFactor2 to hold an AI championship with custom teams, modifications and strategies

# Requirements
There are bare minimum requirements game must be satisfied in order to hold said championship. These requirements are:
```
Zmiana danych kierowców i ich statystyk
Zmiana nazw zespołów 
Zmiana specyfikacji bolidów
Ustawione z góry strategie pit stop
Zarządzanie awaryjnością bolidów
```
# Environment
- Windows 10
- https://steamcommunity.com/sharedfiles/filedetails/?id=1515650133&searchtext=f1
- rFactor2 v.1.1134
- GMotor2 MAS File Utility v2.94
# 'Is it possible (in a fairly easy way)?' list:
- Driver
	- [x] Change personal data i.e. 
		- [x] Frist Name
		- [x] Last Name
		- [x] Number
		- [ ] Nationality (PROBABLY NOT)
	- [ ] Change personal statistics i.e.
		- [x] Determine what these statistics are
			Based on F1 1975 mod there are:
			-  Aggression=90
			- Reputation=70
			- Courtesy=18
			- Composure=87
			- Speed=92
			- Crash=9
			- Recovery=39
			- CompletedLaps=99
			- MinRacingSkill=78
			What they change is yet to be determined

- Car
	- [x] Change paintjob
	- [ ] Set individual pitstops (Kinda possible with adding right amount of fuel)
	- [x] Change individual statistics i.e.
		- [ ] Determine what these statistics are
- Team
	- [x] Nationality in f1 2013 component you can do that, but rfactor2 doesn't show nationality (at least I didn't notice it)
	- [x] Name
- Game mechanics
	- [x] Run AI-only race
		You can add Pan Kamerzysta and this will suffice. Another issue is to do it seamlessly. Now it takes me too many tries to feel the system out
		
	- [x] See a replay without breaking game
		Looks like its possible with one anomaly similar to AM2
	
	- [ ] Get rid of Pan Kamerzysta (ABSOLUTELY NOT)
# Observations along the way
## Component conversion
if your installed package has `something.mas` file and `encrpyted.something.mas` 
then conversion will be impossible since it will (don't know how yet) detect it has been repackaged. Even without encrypted mas file.
## Replays
- Tyres (at least the colour) are same as they were when you hit replay even when viewing incident before pitstop i.e. 
  S -> pit stop -> M 
  but in replay will be
  M -> pit stop (blink for a second of S) -> M
## Components
Even when repackaged without changing anything i.e.:
- extracted files
- created new .mas file
- created component based on that .mas file
- installed 
## Autmoation
https://github.com/nlhans/MAS2Extract NOT TESTED YET
someone wrote a utility to extract MAS files, the code could also be reversed to automate packaging new components.

Case shown below is with mod https://steamcommunity.com/sharedfiles/filedetails/?id=1515650133&searchtext=f1. It is yet to be determined what is different, but same steps with mod https://steamcommunity.com/sharedfiles/filedetails/?id=1254885809&searchtext=F1+ASR+2017 it is possible and you can change, names, numbers teams. Knowing that this method of editing is working the task now is to find mod with more customizable elements AND find out why Mika Hakkinenn mod doesn't allow for the same procedure
```
The game recognizes component as a workshop item although it seems that it doesn't override it.

When modified (only name of one driver) game did not tried to update the mod, but the mode is not available from content manager menu

When component exported to .rfcmp was installed from gMotor2 it did work only at the first time. Next version for some reason couldn't be installed although it was showing that it indeed was installed. Moved .rfcmp file to $rfactor2_root/Packages/ and isntalled from ModManager.exe. rFactor2 now recognizes the mod and current version, BUT for some reason car CAN NOT be selected from race prep view.
```
 
## Controls
`i` Give up control to AI 
`del` (bind) Pit Menu 
`home`  `end` `ins` change camera
`r` replay
`p` pause
`u` free camera (in locked views)

---
# Nomenclature
### Component
A one mod, element, like custom car, track, UI add.
File (.rfcomp)—this is a single element of a MOD. A component contains all the .mas files that were needed to create a single track, vehicle, etc.
### Mod
Bundle of **Components** versioned and signed. Useful for esport where everyone needs the same bundle of components installed. Mod is defining what cars and will be used in session. Can't run a server without a mod file. 
File, (.rfmod)—this contains all of the signed components that it requires. If a MOD consisted of 2 tracks and 3 cars then it would have at LEAST 5 components packed in it, if not more due to sound, UI or other elements

## MAS file
MAS file, (.mas)—a file that contains some or all of the loose files that create a particular asset, be it a vehicle, track, sound pack, etc. This should be very familiar to you if you did previous modding for rF1

## GMT file
.gmt files are (from what I could gather) 3d model of car. RThere seems to be an issue converting those files from rfactor 1 to 2
https://forum.studio-397.com/index.php?threads/tutorial-how-to-quickly-and-efficiently-bring-a-rf1-mod-over-to-rf2.67508/


# Tutorials, Guides and other helpful resources
- https://www.youtube.com/watch?v=qoc4gI6gSIc&list=PLGxM1fwXPGq5fcFHMNg7iv0tBD_k6DzD8
- https://forum.studio-397.com/index.php?threads/tutorial-rfactor-2-car-modding-mas-editing-skin-livery.57317/
- https://www.studio-397.com/wp-content/uploads/2016/12/rF2_Packaging_Tutorial.pdf
- http://devblog.ctdp.net/2012/06/getting-started-to-package-a-rfactor2-mod/
- https://youtu.be/0zgwpICYilU

# Tools
## Mod Manager System
Path: `C:\Program Files (x86)\Steam\steamapps\common\rFactor 2\Bin64\ModMgr.exe`
Version used in this guide: 0.93x

The basic premise for mod manager system is to move selected components of selected mod to `$rfactor2_root/installed` directory.

It shows a dependency tree 

`Working Dir` must be the rFactor2 root
`Package Dir` must be inside the rFactor2 root

## gMotor2 MAS File Utility
Path: `C:\Program Files (x86)\Steam\steamapps\common\rFactor 2\Support\Tools\MAS2`
Tool for managing components i.e. where you modify your car, player, etc.
Use the tool to extract files you want later modify

## MAS Extraction tool
https://forum.studio-397.com/index.php?threads/right-click-mas-extraction.61876/
https://forum.studio-397.com/index.php?attachments/extract-zip.19434/
havben't installed it yet (there's a chance it's a virus XD)
# Troubleshooting
When mod is not visible- restart
If you get error joining rf2 server, verify files integrity from steam
