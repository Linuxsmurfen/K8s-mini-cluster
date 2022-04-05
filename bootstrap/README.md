How to setup a 3 node cluster using



1. Download Ubuntu 20.04 LTS and create a USB boot stick
2. Starta a small webserver 'python3 -m http.server 8080' to publish the data in the autoinstall directory
3. Boot the server and halt the installer and change the Grub to use autoinstall settings.

~~~
setparams 'Install Ubuntu Server'

     set gfxpayload=keep
     linux  /casper/linux autoinstall  "ds=nocloud-net;s=http://<IP>:8080/"  ---
     initrd /casper/initrd
~~~
(needed to set FN+NUMLOCK and enter '0' to get a '-' sign)




