How to install the SSH Tunneling</br>
Download, adapt and install the template script for initiating autossh</br>
git clone https://github.com/benax-rw/SSH-Tunneling</br>
Note: autossh_rca001.sh has been adapted from the original one that was written by Clément Désiles.</br>

</br></br>
Have a look at it and see whether we need to make some changes regarding the Tunnel Port, username, IP address of the server (VPS in our case) or anything else.</br>
sudo nano SSH-Tunneling/autossh_rca001.sh</br>
</br>

Well, now being satified with our autossh script, let's install it in our system</br>
sudo mv SSH-Tunneling/autossh_rca001.sh /etc/init.d/autossh</br>
sudo rm -r SSH-Tunneling</br>
sudo chmod +x /etc/init.d/autossh </br>
sudo update-rc.d -f autossh defaults 90 90 > /dev/null 2>&1</br>
</br>
Reboot for the installation to take effect</br>
sudo reboot</br>
