# helps

# ubuntu uk keybord layout
setxkbmap -layout gb  

# start mongo database
sudo service mongod start

# pep-8 cheetsheet
https://www.slideshare.net/p3infotech_solutions/python-programming-essentials-m31-pep-8

# processes which use gpu
sudo fuser -v /dev/nvidia*
# kill all the processes which use GPU
kill -KILL `sudo fuser -v /dev/nvidia*`

# bash previous command repeat/output
!! or `!!`



# Ubuntu Nvidea drivers
Using 18.04+ To install run the following command:

sudo add-apt-repository ppa:graphics-drivers/ppa
This will automatically update the repositories and then you can run the following line:

sudo apt install nvidia-driver-396
If your desktop does not load after installing the corresponding driver, then do the following:

sudo nano /etc/gdm3/custom.conf
then remove the comment (# symbol) from the line that says
WaylandEnable=false
and save. Then reboot. If this still does not work, then please disable Secure Boot since you might actually be using UEFI.





