# VirtualBox - Notes

---
## Ubuntu VM
### Installation
In VirtualBox:
- Select `New`
  - Name the VM, select the installation directory, type and version of the VM
  - Choose the available memory
  - Choose drive, usually stick to the default setting of `create drive`
  - Filetype of the drive: Select `VDI`
  - Type of storage: `dynamically allocated` (Stick to the default)
  - Set the size of the drive, usually 20 or 50 GB, depends on the needs of the VM
  - Enter `Create`
- Edit the created VM
  - `General` | `Advanced`: Selet `bidirectional`
  - `System` | `CPU`: Set to number of vCPUs that should be used by the VM
  - `Display` | `Screen`: Set the GPU storage to the maximum
  - `Storage` | `Controller: IDE`: Select the `empty` slot and via the CD select the iso-file of the Ubuntu OS
- Now start the VM and complete the installation setup of Ubuntu
- After the setup, the Ubuntu VM will be not in fullscreen even if the VM window of VirtualBox is set to fullscreen

### Enable fullscreen mode
In VirtualBox:
- Go to Settings | Additional Pakets 
  - Add the `Oracle VM Virtualbox Etension Pack`
- Start the VM (should start not in fullscreen mode, even when the VM window is in fullscreen)

In the VM:
- Install the `Guest Additions`
- Open the `Guest Additions` drive and execute ``
- Restart the VM and it should start in fullscreen mode

---
## Kali Linux
### Installation
[Kali Linux is available as `.ova` or `.vbox` file](https://www.kali.org/get-kali/#kali-virtual-machines) which can be [direclty imported into VirtualBox](https://www.kali.org/docs/virtualization/import-premade-virtualbox/). 
After this import, the Kali VM will be automatically created and available. 

To import the `.ova` file:
- Go to File | Import appliance
  - Select the `.ova` file and continue
  - Edit the default values and import after accepting any licence agreements

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
## Move VM files on host machine (Windows)
From version 6.x just use the contxt menu of the VM that should me moved, and select `Move` to choose the new target directory. 
Also snapshots are moved with this option. 
