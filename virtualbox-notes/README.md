# VirtualBox - Notes

---
## Ubuntu VM
### Installation
...

### Enable fullscreen mode
...

---
## Increase the drive space of a virtual machine
The VM has to be turned off. 

In VirtualBox:
- Go to File | Manager for virtual drives
  - Choose VM to increase space
  - At attributes: increase the size for `.vdi` and each snapshot
- Start the VM

In the VM:
- The VM still has not the enlarged space
- Install [gparted](https://wiki.ubuntuusers.de/GParted/) via `sudo apt-get install gparted`
- Open `gparted` to add not allocated space to drive
  - Select the smaller partition and via `Resize/Move the selected partition` increase the size
  - Apply the changes
- Restart the VM

---
## Shift VM files on host machine (Windows)
...
