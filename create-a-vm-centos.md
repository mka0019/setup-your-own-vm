# Create a VM lab

## Your first VM > Ubuntu

What OS is your VM running?

It's running CentOS Stream 9


What challenges did you face while creating your VM? What troubleshooting steps did you take to resolve those challenges and what did you research?

> The mouse was in VB was not working and caused entire mac to freeze. After shutting my computer down. I went to settings > system > pointing device > USB Tablet. This did the trick! 

> Learned that apt doesn't work for centOS. Instead I had to run the following commands:

sudo dnf update >> dnf is centos's equilvant to apt

sudo dnf install bzip2 build-essential gcc make perl dkms >> This didn't work, because build-essential and dkms was not found.
Ran these commands instead:

sudo dnf groupinstall "Development Tools"
sudo dnf install epel-release
sudo dnf install dkms
sudo dnf update -y
sudo dnf install dkms perl bzip2 -y




How much RAM and hard disk space did you allocate to your VM? Why did you choose these amounts?

> RAM > 4096MB and HARD DISK > 32 GB. 
> These settings were choosen because they were recommended for the best performance. 


What do you think would happen if you allocated too much RAM to your VM?

> Allocating to much RAM, might slow down the host system, which I think what was causing my laptop to crash. It might even cause instability of the host runs out of memory. 


What settings did you change and why?
> Tried chaniging the 3D Acceleration with centOS for better grahics, unfortunately, it also crashed. 


How did your VM perform before and after changing the settings?
> Will need to test this on Windows, unfortunately Mac doesn't support the above. 


What other settings do you think could be important for optimizing a VM’s performance?

> Perhaps increase CPU count. Increase in CPU count allows multi-tasking. 