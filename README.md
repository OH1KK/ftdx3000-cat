# ftdx3000-cat
Shell script to command Yaesu FTDX-3000 rig

ftdx3000-cat  {poweron|poweroff|30-56000|lsb|usb|cw|readfreq|readsig|tune|vol000 - 255}

See CAT commands: https://www.yaesu.com/downloadFile.cfm?FileID=8925&FileCatID=158&FileName=FTDX3000%5FCAT%5FOM%5FENG.pdf&FileContentType=application%2Fpdf

## Install

* download script
* edit script, modify script to match your serial port and cat baudrate
* copy script to /usr/local/bin
* give execute permissions   chmod a+rx /usr/local/bin/ftdx3000-cat

## Usage

Turn on radio

    ftdx3000-cat poweron

Tune to 3699kHz

    ftdx3000-cat 3699

Change mode to LSB

    ftdx3000-cat lsb
   
Change volume to reasonable level

    ftdx3000-cat vol100

## Troubleshoot

Make sure you have access to serial ports, add yourself to dialout group

   sudo adduser USERNAME dialout
   
Where username is your user account

## Licence

GPLv3
