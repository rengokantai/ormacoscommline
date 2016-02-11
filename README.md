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
- 5-4
```
sudo /usr/sbin/systemsetup -getstartupdisk
!! //last cmd
sudo /usr/sbin/systemsetup -liststartupdisks
sudo /usr/sbin/systemsetup -getdisplaysleep
sudo /usr/sbin/systemsetup -getcomputername
sudo /usr/sbin/systemsetup -setcomputername newname
```

- 5-5
```
sudo /usr/sbin/networksetup -listallnetworkservices
sudo /usr/sbin/networksetup -listnetworkserviceorder
sudo /usr/sbin/networksetup -listallhardwareports
sudo /usr/sbin/networksetup -getmacaddress en0
```

- 6-1
```
/usr/sbin/softwareupdate --help
/usr/sbin/softwareupdate -l   //list all sw need to update
/usr/sbin/softwareupdate -v -i swname  //update
/usr/sbin/softwareupdate -v -i -a   // install all. need to restart computer
```

- 6-2
power management
```
pmset -g live
pmset -g cap
pmset -g stats
pmset -g logs
pmset -g ups
pmset -g everything
sudo pmset -a key1 value1 key2 value2
sudo pmset restoredefaults
```
- 6-3
reset apple assistant
```
sudo rm /var/db/.AppleSetupDone
```
- 6-4
create full install media set (download install OS X Yosemite.app first) erase first.
```
cd ~/Desktop/Instal\ OS\ X\ Yosemite.app/
sudo ./createinstallmedia --volume /Volume/Untitled\ 1/ --applicationpath ~/Desktop/Instal\ OS\ X\ Yosemite.app
```

- 7-1
Finder->Go->Utilities->Disk Utility  
partition-> options-> MBR, apple partition map
```
diskutil list

system_profiler SPStorageDataType
```

```
cd /Volumes/
```
- 7-2 split
```
diskutil partitionDisk
```
```
diskutil partitionDisk /dev/disk1 2 MBR fat32 MBR1 50% fat32 MBR2 R  (remainder)
```

split partition.(all data will be lost)
```
diskutil splitPartition
```
```
diskutil splitPartition /dev/disk2s3 2 JHFS+ APM1 4G JHFS+ APM2 3.9G
```

```
diskutil resizevolume  //does not destroy data
```
  
- 7-3 merge partitions
```
diskutil mergePartitions fat32 MBR disk1s1 disk1s2
diskutil mergePartitions jhfs+ APM disk2s3 disk2s4      //delete 2nd partition
```

