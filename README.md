# Dualboot-guide
How to install both Windows and Linux on a machine.

1. Partitions needed: 
    1x ntfs -> Windows, at least 100 GB
    2x swap, at least 2 GB, sizes depending on your RAM
    1x ext4 ->Ubuntu, at least 50 GB
    
2. USB Stick 8+ GB
If you have Windows, use Rufus, else use unetbootin

   -ntfs for booting Windows
   -fat32 for Ubuntu
   
3. Installing

On booting press F12, Esc, F10, Enter
   - select Boot from USB 

Ubuntu
   - follow the steps, until you reach this step and  select last option
      https://www.google.com/url?sa=i&url=http%3A%2F%2Fwww.askaswiss.com%2F2017%2F01%2Fhow-to-install-ubuntu-16-04-alongside-windows-10-dual-boot.html&psig=AOvVaw1Ccf72hT9lMoDdPUn8mbgC&ust=1593272642861000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCLjDwaTpn-oCFQAAAAAdAAAAABAD
   - !! select only ext4 partition, go further and accept everything
   - in case you cant go further, delete the ext4 partition and create a new one
   
Windows
   - follow the steps until you get here, and then select Custom
   
   - !! select only the ntfs partition and go further


__Splitting Your Partitions
    Ubuntu
        - install gparted: sudo apt-get install gparted
        - !! if you have only one partition, you will have to split the partitions via terminal -> tutorial: https://opensource.com/article/18/6/how-partition-disk-linux
        - make the needed partitions and save
        
    Windows
        - rightclick on My Computer and go to properties
        - go to partitions and add 1 swap and 1 ext4 partitions
