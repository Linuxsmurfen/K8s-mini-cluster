How to setup a 3 node cluster using



Download Ubuntu 20.04 LTS and create a USB boot stick  
Boot the server and halt the installer and change the Grub to use autoinstall settings.

setparams 'Install Ubuntu Server'

     set gfxpayload=keep
     linux  /casper/linux autoinstall  "ds=nocloud-net;s=http://192.168.1.111:8080/"  ---
     initrd /casper/initrd
     

(needed to set FN+NUMLOCK and enter '0' to get a '-' sign)


Make sure that a webserver is up and running with the content
Use a small webserver 'python3 -m http.server 8080' in the autoinstall directory

