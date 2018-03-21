# ftdx3000-cat
Shell script to command Yaesu FTDX-3000 rig

ftdx3000-cat  {poweron|poweroff|30-56000|lsb|usb|cw|readfreq|readsig|tune|vol000 - 255}

See CAT commands: https://www.yaesu.com/downloadFile.cfm?FileID=8925&FileCatID=158&FileName=FTDX3000%5FCAT%5FOM%5FENG.pdf&FileContentType=application%2Fpdf

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

Turn on radio

    ftdx3000-cat poweron

Tune to 3699kHz

    ftdx3000-cat 3699

Change mode to LSB

    ftdx3000-cat lsb
   
Change volume to 40% level

    ftdx3000-cat vol40

## Troubleshoot

Make sure you have access to serial ports, add yourself to dialout group

    sudo usermod -a -G dialout user
   
## Licence

GPLv3
