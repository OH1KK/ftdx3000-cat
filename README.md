# ftdx3000-cat
Shell script to command Yaesu FTDX-3000 rig

```
ftdx300-cat Yeaesu FTDX-3000 commander

/usr/local/bin/ftdx3000-cat command

Where command in
30.0 - 56000.0	set VFO A frequency
vol0 - vol99	change audio volume 0-99%
poweron		Power on rig
poweroff	Power off rig
readmode	read mode
readsig		read signal meter
readfreq	read VFO A frequency
readsql		read squelch value
sql0 - sql99	set quelch value
lsb		set mode
usb		set mode
cw		set mode
fm		set mode
am		set mode
fsk		set mode
cw-r		set mode
pkt-l		set mode
fsk-r		set mode
pkt-fm		set mode
fm-n		set mode
pkt-u		set mode
am-n 		set mode
```

## Requirements

* Linux computer, for example Raspberry Pi
* Yaesu FTDX-3000 radio
* USB-cable between rig and computer

## Install

    git clone https://github.com/OH1KK/ftdx3000-cat.git

Edit script with your favourite text editor. Update file to match your serial port and CAT-baud rate.

    vi ftdx3000-cat/ftdx3000-cat 
    
Then copy script to /usr/local/bin and give execute rights to it

    sudo cp ftdx3000-cat/ftdx3000-cat /usr/local/bin
    sudo chmod a+rx /usr/local/bin/ftdx3000-cat

## Usage

Power on the radio

    ftdx3000-cat poweron

Tune to 3699kHz

    ftdx3000-cat 3699

Change mode to LSB

    ftdx3000-cat lsb
   
Change volume to 40% level

    ftdx3000-cat vol40

## More info

Download FTDX3000 series CAT Operation Reference Book from Yaesu web site: https://www.yaesu.com/downloadFile.cfm?FileID=8925&FileCatID=158&FileName=FTDX3000%5FCAT%5FOM%5FENG.pdf&FileContentType=application%2Fpdf

## Troubleshoot

Make sure you have access to serial ports, add yourself to dialout group

    sudo usermod -a -G dialout user

## Licence

GPLv3
