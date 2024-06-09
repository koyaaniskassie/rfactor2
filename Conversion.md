# Environment
- Windows 10
- rFactor2 v.1.1134
- Component https://www.dropbox.com/scl/fi/cm246693jqwd1zn8vn152/Formula-1%202013.rar?rlkey=g7mx9pwb8q92mrpdxckw2zfpt&e=1&dl=0
- gMotor2 MAS File Utility v2.94 `$rfactor2_root/Support/Tools/MAS2.exe`
- rFactor2 Mod Manager v0.93x `$rfactor2_root/Bin64/ModMgr.exe`

# Tutorial
1. Download F1 2013 rar from https://www.dropbox.com/scl/fi/cm246693jqwd1zn8vn152/Formula-1%202013.rar?rlkey=g7mx9pwb8q92mrpdxckw2zfpt&e=1&dl=0
2. Extract F1RFT_2013_Frenky_1.64.rfcmp to `$rfactor2_root/Packages`
3. Open Mod Manager
	1. Install component F1RFT_2013_Frenky_1.64 ![[31.png]]
4. Open gMotor2 editor
	1. Open `$rFactor 2_root\Installed\Vehicles\F1RFT_2013_Frenky_1.64/1.64`
	2. Drag `$TEAM_TEAMMAS.mas` file to gMotor2 editor
	3. Extract `*.VEH` file ![[43.png]]
	4. Edit Name, Number etc. These files contain descriptive items for team's driver (driver's and car's stats will be changed later)
	5. Save  your changes
	6. Drag edited .VEH files to gMotor2
	7. Save (overwrite existing file)
5. In gMotor2 editor click `create the package file` icon (it's right under `View` menu looks like half-open box)
	1. Choose `Create Single Cmp Package`
	2. Click `Edit component Name` and choose name for your package (in this tutorial it'll be `f1_2013`)![[52.png]]
	3. Click `Select location for component`![[53.png]]
	4. Choose Version `1.0` and Type `vehicle` (it's only informative but, it's better to have it)
	5. Select MAS files to include in package (include all of them)![[55.png]]
	6. Click `Package`. This will create .rfcmp file in `$rfactor2_root/Packages` directory
6. Open Mod Manager
	1. Refresh if it was running before fifth step
	2. Look for `Component` with name, in this case, `f1_2013` and select it
	3. Click `Install`
	4. If you click again on this component you'll see list of .mas files this component has
7. Run rFactor2

**File for driver's stats is in `F1RFT2013_TALENT.mas` `F1RFT2013.RCD` . Don't know how it connects to the driver. Tested it by lowering stats to Bottas and he was loosing 4 seconds a lap so stats make a difference.**

**File for aero is in `$(TEAM_SHORTCUT)_UPGRADES.INI` file in `$(TEAM)_TEAMMAS.mas`**



# TODO
## How to add more drivers
---

## How to tie custom named driver to statistics in `F1RFT2013_TALENT.mas`
---

## Find engine stats file
---
Found ENGINE.INI in `F1RFT2013_v161.mas` file but can't find what points to that file. 
There are few other GEN INI and TXT files in mas files that are not related to any team. Their purpose and how to use them is yet to be determined

