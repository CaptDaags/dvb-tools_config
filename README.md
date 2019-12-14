# dvb-tools_config
Config files for use with dvb-tools and realtec USB receiver

This was built by information contained on the CWNE88 You Tube channel located at https://www.youtube.com/watch?v=asmCMmq06R0

Check Your Tuner Dongle:
Plug in the dongle
Run ls /dev/dvb to see if you see an adapter0
To make sure you run dmesg and see that the adapter is in "warm state" if so all good to continue

If you dont have the adapter0 then run dmesg and if it is in "cold state" then its probably missing drivers. You will need to find the firmware and drop it in /lib/firmware and boot the box.


To install:
sudo apt-get install dvb-tools

To build the channels file:
Go to /usr/share/dvb/dvb-t or /usr/share/dvb/dvb-legacy/dvb-t you will find the city files. You need to look for au-Melbourne files and cp to ~/

With the tuner plugged in and connected to an antenna, do a scan au-Melbourne and it will scan the city file. You will see the output. To make it into a file by scan au-Melbourne > channels.conf

You can then open that channels.conf file with VLC and then watch the channel.
