# kvm-setup

---------------------------------
Ubuntu on MSI Leopard 8R3 (MS-16P5)
i7-8750H 2.2GHz 6 cores / 12 threads

32Gb
---------------------------------
Ubuntu 18.04.1 hangs unless a few settings are disabled:
<p>BIOS config:
<br>Intel SpeedStep: enabled
<br>ERP lot 3 support: enabled
<br>Wake up on LAN S5 support: disabled
<br>Win/Fn Key Swap: disabled
<br>BACKSLASH/ALT Key Swap: disabled
<br>Network Stack: disabled
<br>Inter Virtualization: enabled
<br>VT-d: enabled
<br>Hyper-threading: enabled
<br>CPU C states: <b>DISABLED</b>
<br>Fast Boot: enabled
<br>Boot Mode: UEFI
<br>Secure Boot: <b>DISABLED</b>

<p>Grub: nouveau.blacklist=1 acpi=off


NVIDIA
<br>ubuntu-drivers devices --> GP106M GeForce GTX 1060 mobile nvidia-driver-<b>390<b>
<br>sudo apt-get purge nvidia*
<br>sudo add-apt-repository ppa:graphics-drivers
<br>sudo apt-get update
<br>sudo apt-get install nvidia-390
<br>sudo apt-mark hold nvidia 390
