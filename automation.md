ModMgr.exe CLI options

# Sources
https://forum.studio-397.com/index.php?threads/rfcmp-cli-tooling.67452/

# Packaging MAS files as Component
## .dat files
Descriptive files used to create new mod or package.

# Extracting and packaging regular files to MAS files
## Extraction
```
ModMgr.exe -x"C:\rf2_files\F1_2012\mas\F1_Caterham_2012_MAIN.mas" Caterham_Upgrades.ini Caterham_Cams.cam
```
Current issue is that I can't redirect output i.e. wherever you run your command, there you'll get these files extracted. Option `-o(utput)` doesn't work.

## Packaging
Package:
`ModMgr.exe -m"new_caterham.mas" Caterham_*`

Check for files:
`ModMgr.exe -lnew_caterham.mas`
## Component
The most basic .dat file for component contains
```
[Component]
Name=Caterham
Type=2
Version=1.0
BaseVersion=
MinVersion=
Author=
Date=0
ID=
URL=
Desc=
Category=3
Origin=0
Flags=0
CurLocation=0
NumLocations=1
Location=C:\Program Files (x86)\Steam\steamapps\common\rFactor 2\Packages\caterham.rfcmp
NumMASFiles=2 
MASFile=C:\rf2_files\F1_2012\mas\F1_Caterham_2012_MAIN.mas
MASFile=C:\rf2_files\F1_2012\mas\F1_Caterham_2012_MAPS.mas
rFmFile=
IconFile=
SmallIconFile=
```
Most important elements are:
```
NumLocations=1
Location=C:\Program Files (x86)\Steam\steamapps\common\rFactor 2\Packages\caterham.rfcmp
NumMASFiles=2 
MASFile=C:\rf2_files\F1_2012\mas\F1_Caterham_2012_MAIN.mas
MASFile=C:\rf2_files\F1_2012\mas\F1_Caterham_2012_MAPS.mas
```
This setup tells ModMgr to take **2** .mas files defined as separate `MASFile` entries and save it as `caterham.rfcmp` in given location.

Then run command:
```
ModMgr.exe -b"C:\rf2_files\F1_2012\dat\caterham.dat" 0
```
Where 0 points to first `[Component/Mod]` since you can define more than one in .dat file
# Goal
Now, knowing it's possible to automate entire process, write a script that will:
- Pack all regular files to as .mas files
- Pack .mas files as components
- Pack components as versioned mod as a standalone pack for each GP
