# jptvwatchingLinux


2024/7/11.

I rewrite Da point of Da Watta Needed for JPTV watching via LINUX.

[This editor automatic fook recognize caused some weird command line display of no next line like, sudo apt install make
sudo apt install gcc is just fook, ignore.
]


@@@@@@@@@@@@@@@@@@hardware
-sampa
-card reader


@@@@@@@@@@@@@@@@@@1st installing, for scanning, Re install and Re checking Da status.
sudo apt install pcscd

pcsc_scan


@@@@@@@@@@@@@@@@@@other software
*cannot be used another os's executable to another os! PLEASE Re install these !

sudo apt install make
sudo apt install gcc

-b25, 2nd install
sudo apt install git make gcc g++ pkg-config libpcsclite-dev pcscd

cd aribb25
make clean
make
sudo make install

-recfsus, 3rd install

cd src
make clean
make B25=1
sudo make install



*Please do not break Da source code of these, yes re search in Web and get again
Da source is still okay but not so good option, please use Da reliable already successful
source and re use these.





@@@@@@@@@@@@@@@@@@group video accessible to n'able usb as sampa, by add udev rules.
1st, make sure wata sampa in LSUSB command.
typically , sampa = n'able computer.


2nd, add Da info to udev rules, which specify which devices can be accessible by which group.
1. exec this.
sudo vi /etc/udev/rules.d/90-sampa_loader.rules // file add and edit. 
2. copy this.
SUBSYSTEM=="usb", ENV{DEVTYPE}=="usb_device", ATTRS{idVendor}=="0511", ATTRS{idProduct}=="0045", MODE="0664", GROUP="video"

” will be fail instead of "


3. i for edit mode
4. ctl shift v for paste 
5. esc for command mode 
6. : x enter, for save. 
————how to del line 
esc to command mode dd enter 

8. reboot needed! 
or
sudo udevadm control --reload-rules && sudo udevadm trigger



@@@@@@@@@@@@@@@@@@@@@@@@@@@testing

udevadm info /dev/bus/usb/001/006, [change da number for appropriate one by lsusb]
get Da devpath, then

udevadm test /devices/pci0000:00/0000:00:14.0/usb1/1-5/1-5.4 , [this is devpath]


/etc/udev/rules.d/90-sampa_loader.rules:1 Invalid key/value pair, ignoring.                                                                 
/etc/udev/rules.d/90-sampa_loader.rules:2 Invalid key/value pair, ignoring.    

Seeing this is not good......




@@@@@@@@@@@@@@@@@@add self to group video
if not you in group video yet, do it.

cat /etc/group

(group name):x:(id):Members

if video there, but no one inside, do adding me to video

sudo usermod -a -G examplegroup exampleusername


@@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@









21, fuji
22, tbs
23, tele tu
24, tele ass
25, nifun tv
26, nhk e.
27, nhk

30, chiva tele
16, or 20, tk mx

32, tv saitam


101, bs1
103, bs3
141, bs4
151, bs ass-hole
161, bs6
171, bs7
181, bs8



recfsusb2n --b25 27 - - | vlc - --quiet





