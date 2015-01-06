###I2Pberry

VJ2.1.1r1: https://github.com/m6urns/i2pberry/blob/master/torrents/i2pberry_VJ2.1.1r1.img.zip.torrent?raw=true

MD5: f146043309715027879f98e9b117cc0a

All versions will be distributed via torrent, found in the
torrents directory.

#####Features

   - Fail2ban for login monitoring
   - SSH hardening (changed the port, disabled root login,
     really more of a deterrent)
   - UFW for firewalling

#####Working On

   - Version taking advantage of I2Pd
     - I've been watching the development of i2pd and I'm waiting 
       for their release of an offical ARM port. Once that happens
       VC1.0 will be relased, hopefully performance will
       be greatly improved.
   - Onion routeresq plug n play easiness
   - Some integration with ufw so ports don't have to be opened 
     manually
     - Maybe some kind of integration with the intial bootstrap
       script giving you the option to open extra user selected
       ports
   - Automate opening console to network traffic, with user input.

I love suggustions!



###Setup

   user:raspberry

1. Download the image and write it to your SD card. 4 GB is the recommended minimum.
   You can get away with two if you want.

2. Connect to your raspberry either through SSH or physically.

3. Use raspi-config to 
   
   - Expand your SD card.
   - CHANGE YOUR PASSWORD!
   - Dial down your overscan (16)
   - Overclock if you want
   
   Reboot.

4. Use i2p-bootstrap to setup your installation. The script is located in
   /usr/bin It must be run as root. 
   Allow it to do it's thing, respond intelligently to prompts.

5. Lynx will open, configure your bandwidth and any other settings.

   You will now need to login on the 2121 SSH port. Due to "hardening". Also root
   login is disabled on SSH. So you will need to use user.

6. You may need to configure /var/lib/i2p/i2p-config/clients.config to allow local 
   network access. If you do, use a PASSWORD! (Configure that from the webui)
   
   Comment out this line:
   
   ```
   clientApp.0.args=7657 ::1,127.0.0.1 ./webapps/
   ```
   And uncomment this line:
   
   ```
   #clientApp.0.args=7657 0.0.0.0 ./webapps/
   ```

  If your having trouble with the connecting to the webui through the fire wall 
  you can open a port to traffic using 

  ```
  sudo ufw allow 7657
  ```
  Because of the firewall, you need to manually open ports, the process is identical
  to what is detailed above, only the port will change.
