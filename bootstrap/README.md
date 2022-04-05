# Setup the servers



## Install the OS
1. Download Ubuntu 20.04 LTS and create a USB boot stick
2. Starta a small webserver 'python3 -m http.server 8080' to publish the data in the autoinstall directory on the bastion server.
3. Boot the server and halt the installer and append the autoinstall settings to the grub menu.

~~~
setparams 'Install Ubuntu Server'

     set gfxpayload=keep
     linux  /casper/linux autoinstall  "ds=nocloud-net;s=http://<IP>:8080/"  ---
     initrd /casper/initrd
~~~
   (might need to set FN+NUMLOCK and enter '0' to get a '-' sign)



## Configure the OS
1. 

