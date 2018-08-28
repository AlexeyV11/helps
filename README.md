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



