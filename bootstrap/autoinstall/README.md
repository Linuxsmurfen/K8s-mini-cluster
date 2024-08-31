# Install the OS using iPXE boot 
1. Configure netbootxyx, add the following files to the local assets.  
   /boot/ubuntu/meta-data  
   /boot/ubuntu/user-data
   
2. Adjust the 'user-data' file
3. In Proxmox you may have to change boot order under "options" to do a netboot.
4. When booting the server/vm select...  
   Distributions --> Linux Network Installs (64-bit) --> Ubuntu 24.04 LTS --> Specify preseed/autoinstall url --> http://\<FQDN\>:3001/boot/ubuntu/
