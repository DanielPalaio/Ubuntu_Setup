# Ubuntu - Step by step tutorial to install Ubuntu desktop

**1.** Download Ubuntu's .iso image file https://ubuntu.com/download/desktop

**2.** Download Rufus bootloader tool https://rufus.ie/, and create a bootable portable flash drive with the parameters depicted in the following image:

<p align="center">
  <img width="300" height="415" src="https://user-images.githubusercontent.com/79323290/115305210-e7ec8500-a15d-11eb-8d0b-4d48e8f17c24.png">
</p>

**3.** From the boot menu (Reboot PC and press Esc, F2, F10 or F12 key), choose the option to boot from the flash drive

**4.** Choose the language and select the option **Try Ubuntu**

**5.** Open the Ubuntu Terminal to edit the grub (GRand Unified Bootloader) file:  
>$ sudo nano /etc/default/grub  
>Change **GRUB_CMDLINE_LINUX_DEFAULT="quiet splash"** to **GRUB_CMDLINE_LINUX_DEFAULT="quiet splash nomodeset noacpi"**

**6.** Open the desktop shortcut **Install Ubuntu**, select the keyboard layout, and connect to the internet  

**7.** Select **Normal Installation** and checkmark both other options: **Download updates while installing Ubuntu** and **Install third-party software for graphics and Wi-Fi hardware and additional media formats**  

**8.** In the **Installation type** section, choose:  
>**8.1** **Erase Ubuntu and reinstall** to format disk and install Ubuntu as the only Operative System  
or  
>**8.2** **Something else** to keep other Operative Systems already installed  
>>**8.2.1** Delete the non-ntfs type devices to arrange free space  
>>**8.2.2** **Setup Swap Memory**  
>>>**8.2.2.1** Select **free space** and press the on-screen button **+**  
>>>**8.2.2.2** Define the **size** to **double de RAM**  
>>>**8.2.2.3** Define the **Partition** to **Logical**  
>>>**8.2.2.4** Define the **Location for the new partition** to **Beginning of this space**  
>>>**8.2.2.5** Define **Use as** to **swap area**  

>>**8.2.3** **Setup Root**  
>>> **8.2.3.1** Select **free space** and press the on-screen button **+**  
>>> **8.2.3.2** Define the **size** to **Max**  
>>> **8.2.3.3** Define the **Partition** to **Logical**  
>>> **8.2.3.4** Define the **Location for the new partition** to **Beginning of this space**  
>>> **8.2.3.5** Define **Use as** to **Ext4 journaling file system**  
>>> **8.2.3.6** Define  the **Mount point** to **/**  

>>**8.2.4** Select the previously created **Root**, following **Install now**  

**9.** Select the timezone, fill the required user information, and wait for the installation to complete  

**10.** Reboot PC
