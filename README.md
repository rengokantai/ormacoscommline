#### ormacoscommline

- 2-1
open terminal:
shift+cmd+u and cmd+space

- 2-2
window->save window group
command w //close window.
alt command w //close all window
cmd plus/minus  change font size
cmd I  //open inspector

- 2-3
cmd } {  //next/prev window
cmd t  //new tab
```
$system_profiler
```
cmd d //split window
shift cmd d//unshift d

- 2-4
cmd ,   //profile

- 3-1
```
open -a /Applications/TextEdit.app/ a.txt
open -e a.txt
open -b com.apple.TextEdit a.txt
man -t open > open.ps
```

- 3-2
copy (wrong way)
```
ditto -v(-V) /Library/DesktopPictures/   /Users/ladmin/Desktop/   Wrong! This will cause all items in the folder copied on the desktop
```
copy (correct way)
```
ditto -v(-V) /Library/DesktopPictures   /Users/ladmin/Desktop/   correct.  no slash
```

- 4-1
```
strings ~/filename
xcode-select -p
```

- 5-1
```
system_profiler -listDateTypes
system_profiler SPMemoryDataType
system_profiler -xml -detailLevel full
```
- 5-2
```
/usr/sbin/scutil --get ComputerName
/usr/sbin/scutil --get LocalHostName
/usr/sbin/scutil --get HostName
/usr/sbin/scutil --dns
/usr/sbin/scutil --nwi    //network information
scutil -r google.com  //reachable?
```

- 5-3
```
/usr/sbin/diskutil listFilesystems
/usr/sbin/diskutil list
/usr/sbin/diskutil info disk0
```
