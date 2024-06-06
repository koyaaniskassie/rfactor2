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

# 'Is it possible (in a fairly easy way)?' list:
- Driver
	- [ ] Change personal data i.e. 
		- [ ] Frist Name
		- [ ] Last Name
		- [ ] Number
		- [ ] Nationality
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
	- [ ] Change paintjob
	- [ ] Set individual pitstops
	- [ ] Change individual statistics i.e.
		- [ ] Determine what these statistics are
- Team
	- [ ] Nationality
	- [ ] Name
- Game mechanics
	- [x] Run AI-only race
		You can add Pan Kamerzysta and this will suffice. Another issue is to do it seamlessly. Now it takes me too many tries to feel the system out
		
	- [x] See a replay without breaking game
		Looks like its possible with one anomaly similar to AM2
	
	- [ ] Get rid of Pan Kamerzysta 
# Observations along the way

## Replays
- Tyres (at least the colour) are same as they were when you hit replay even when viewing incident before pitstop i.e. 
  S -> pit stop -> M 
  but in replay will be
  M -> pit stop (blink for a second of S) -> M
 
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
A one mod, element, like custom car, track, UI add
### Mod
Bundle of **Components** versioned and signed. Useful for esport where everyone needs the same bundle of components installed. Mod is defining what cars and will be used in session. Can't run a server without a mod file





# Tutorials, Guides and other helpful resources
- https://www.youtube.com/watch?v=qoc4gI6gSIc&list=PLGxM1fwXPGq5fcFHMNg7iv0tBD_k6DzD8
- https://forum.studio-397.com/index.php?threads/tutorial-rfactor-2-car-modding-mas-editing-skin-livery.57317/

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

# Troubleshooting
When mod is not visible- restart
If you get error joining rf2 server, verify files integrity from steam
