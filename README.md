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
WaylandEnable=false and save. Then reboot. If this still does not work, then please disable Secure Boot since you might actually be using UEFI.

# CUDA install
wget https://developer.nvidia.com/compute/cuda/9.0/Prod/local_installers/cuda_9.0.176_384.81_linux-run
chmod +x cuda_9.0.176_384.81_linux-run
./cuda_9.0.176_384.81_linux-run --extract=$HOME
cd $HOME
sudo ./cuda-linux.9.0.176-22781540.run
sudo ./cuda-samples.9.0.176-22781540-linux.run
sudo bash -c "echo /usr/local/cuda/lib64/ > /etc/ld.so.conf.d/cuda.conf"
sudo ldconfig

# CUDA NN

sudo dpkg -i libcudnn7_7.0.5.15–1+cuda9.0_amd64.deb # download from the official website

# conda create env
conda create -n myenv python=3.6

# vnc desktop setup

install - 
sudo apt-get install gnome-panel gnome-settings-daemon metacity nautilus gnome-terminal

change ~/.vnc/xstartup to -
/# Uncomment the following two lines for normal desktop:
/# unset SESSION_MANAGER
/# exec /etc/X11/xinit/xinitrc

[ -x /etc/vnc/xstartup ] && exec /etc/vnc/xstartup
[ -r $HOME/.Xresources ] && xrdb $HOME/.Xresources
xsetroot -solid grey
vncconfig -iconic &
x-terminal-emulator -geometry 80x24+10+10 -ls -title "$VNCDESKTOP Desktop" &
x-window-manager &

gnome-panel &
gnome-settings-daemon &
metacity &
nautilus &


