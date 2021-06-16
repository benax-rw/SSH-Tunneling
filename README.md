How to install the SSH Tunneling
Download, adapt and install the template script for initiating autossh
git clone https://github.com/benax-rw/SSH-Tunneling
Note: autossh_rca001.sh has been adapted from the original one that was written by Clément Désiles.


Have a look at it and see whether we need to make some changes regarding the Tunnel Port, username, IP address of the server (VPS in our case) or anything else.
sudo nano SSH-Tunneling/autossh_rca001.sh


Well, now being satified with our autossh script, let's install it in our system
sudo mv SSH-Tunneling/autossh_rca001.sh /etc/init.d/autossh
sudo rm -r SSH-Tunneling
sudo chmod +x /etc/init.d/autossh 
sudo update-rc.d -f autossh defaults 90 90 > /dev/null 2>&1

Reboot for the installation to take effect
sudo reboot
