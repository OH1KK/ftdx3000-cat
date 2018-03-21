# ftdx3000-cat
Shell script to command Yaesu FTDX-3000 rig

```
ftdx300-cat Yeaesu FTDX-3000 commander

/usr/local/bin/ftdx3000-cat command

Where command in
30.0 - 56000.0	Set VFO A frequency
+hz		Tune VFO up where hz value, 100 - 10000
-hz		Tune VFO down where hz value 100 - 10000
vol0 - vol99	Change audio volume 0-99%
poweron		Power on rig
poweroff	Power off rig
readmode	Read mode
readsig		Read signal meter
readfreq	Read VFO A frequency
readsql		Read squelch value
sql0 - sql99	Set quelch value
lsb		Set mode
usb		Set mode
cw		Set mode
fm		Set mode
am		Set mode
fsk		Set mode
cw-r		Set mode
pkt-l		Set mode
fsk-r		Set mode
pkt-fm		Set mode
fm-n		Set mode
pkt-u		Set mode
am-n 		Set mode
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

## Usage examples

Power on the radio

    ftdx3000-cat poweron

Tune to 3699kHz

    ftdx3000-cat 3699

Change mode to LSB

    ftdx3000-cat lsb
   
Change volume to 40% level

    ftdx3000-cat vol40

Read frequency

    ftdx3000-cat readfreq
    VFO A is tuned to 1847.200 kHz

Read S-meter

    ftdx3000-cat readsig
    Signal level is S2 - 4% of full scale

## More info

Download FTDX3000 series CAT Operation Reference Book from Yaesu web site: https://www.yaesu.com/downloadFile.cfm?FileID=8925&FileCatID=158&FileName=FTDX3000%5FCAT%5FOM%5FENG.pdf&FileContentType=application%2Fpdf

## Troubleshoot

Make sure you have access to serial ports, add yourself to dialout group

    sudo usermod -a -G dialout user

## Licence

GPLv3
