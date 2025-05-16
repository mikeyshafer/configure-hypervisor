<p align="center">
<img src="https://github.com/user-attachments/assets/c99c8f92-1431-435a-a7ca-4bbdb0885825" alt="game preview"/>

</p>

<h1>Configuring a Type 1 Hypervisor Using an Old Laptop</h1>
As a first step to building out an IT home lab for testing and learning purposes, I configured an old laptop of mine to be a host for multiple virtual machines using Proxmox. In this demonstration I'll briefly show the steps I took to turn my laptop into a server that has 3 virtual machines, with Kali Linux, Ubuntu, and Windows Server 2022 operating systems installed. All are accessed remotely through my main PC on the network, and I can install more VMs if I want to!<br />

<h2>Install Proxmox and Configure Boot Device</h2>
<img src="https://github.com/user-attachments/assets/ab4ca246-3dff-4610-b0cc-126962ff23f8" alt="game preview"/>
<p>
  I first installed Proxmox and used Rufus to configure a USB to use as the boot device on my laptop.
</p>

<h2>Reboot Hypervisor Device Using Proxmox Boot</h2>
<img src="https://github.com/user-attachments/assets/1692a88a-43c2-43c3-9143-7acd641164d5" width=80% alt="game preview"/>

<p>
  Then I connected the USB, now configured as a boot device with Proxmox installed, to my old laptop and restarted it (Make sure there's no important files on the device because the new OS will wipe everything). I opened the boot menu and changed the boot device to USB Hard disk, then went through the Proxmox installer.
</p>

<h2>Proxmox Virtual Environment Setup</h2>
<img src="https://github.com/user-attachments/assets/0da5ed8b-278e-4a34-8577-c15a024d4edf" width=80% alt="game preview"/>

<p>
  In the address bar of my main PC, I typed "https://[my new hypervisor's Private IP]" to load up the Proxmox Virtual Environment where I can operate the hypervisor. To set it up, I ran some shell commands to allow all of the storage space to be used by the virtual machines I will create.
</p>

<h2>Upload ISO Files</h2>
<img src="https://github.com/user-attachments/assets/6465b2f1-8a7a-4250-9569-60a264670a31" width=80% alt="game preview"/>
<p>
  For each OS for which I wanted to make virtual machines, I downloaded their ISO files from the manufacturers' websites. To start, I decided to use Kali Linux, Ubuntu, and Windows Server 2022. Once they were downloaded, I uploaded them to my ISO Images in the environment.
</p>

<h2>Create Virtual Machines</h2>
<img src="https://github.com/user-attachments/assets/d6ed95b9-2078-4bd5-a678-1b504c754e4b" width=80% alt="game preview"/>
<p>
  Once the ISO images are all uploaded, I was able to create virtual machines using each one, and go through the install processes.
</p>

