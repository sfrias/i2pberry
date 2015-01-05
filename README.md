I2Pberry

VJ2.1.1 https://github.com/m6urns/i2pberry/blob/master/torrents/i2pberry_VJ2.1.1.zip.torrent?raw=true
MD5: bd5eade0245aab4c02589df17ca7ee0f

I've been watching the development of i2pd and I'm waiting 
for their release of an offical ARM port. Once that happens
VC1.0 will be relased, hopefully performance will
be greatly improved.

All versions will be distributed via torrent, found in the 
torrents directory.

Setup

1. Download the image and write it to your SD card. 4 GB is the recommended minimum.
   You can get away with two if you want.

2. Connect to your raspberry either through SSH or physically.

3. Use raspi-config to 
   
   - Expand your SD card.
   - CHANGE your password!
   - Dial down your overscan (16)
   - Overclock if you want
   
   Reboot.

4. Use i2p-bootstrap to setup your installation. The script is located in
   /usr/bin It must be run as root. 
   Allow it to do it's thing, respond intelligently to prompts.

5. Lynx will open, configure your bandwidth settings and if you want configure
   I2P so it can be accessed from your local network. If you open it to outside 
   network traffic you really need to put a password on.

