# Acer-Nitro-5-AN515-52-OpenCore-EFI

## What is an Opencore
Opencores focuses on making commercial solutions a open source alternative, in this repo I've focused on building an efi for my specific configuration piece by piece. Opencore acts as a layer that helps you configure the raw mac os for your specific pc by giving you boxes that you could fill with ACPIS, KEXTS, SMBIOS. 

## What's an EFI
An efi is basically a folder or a partition per se that your computer relies on to boot its system up, help it load up its drivers, cross reference its functionalities and parameters.

## How can I you use my EFIs
With great power comes great responsibility, Access to an efi aka gives to access to the bare-bones of your computer, be sure of the kexts that you add inside as they could end up acting as a spy layer. Nothing's perfect a quote by hiromu. In light of that, this efi has been tested for wifi, bluetooth, and Geolocation functionalities. Changing screen brightness, and audio works as you'd expect. There's still a quirk with battery indicator, and the cpu temp module. As you might expect, airdrop, and phone doesn't work whereas facetime seems to be working perfectly. This efi could be used standalone on your computer but I really wouldn't recommend this for a daily driver. This is to serve as a base to you endless testings and to act as a jump pad into errors and compatibility issues waiting to be solved. 

# Installing
Well considering you've decided to throw my prior advice off the window and to just use it and test out what errors it might lead to I've got your back on that too. <strong>Make note that the per-requisites being Python3 has been installed on your pc</strong> <br/>
<h3>1.Downloading macos base system:</h3>
<strong>On Windows</strong>, Start by downloading <a href="https://github.com/acidanthera/OpenCorePkg/releases">Opencore package</a>, and navigating inside <em>/Utilities/macrecovery/</em> and enter the code <em> python3 macrecovery.py -b Mac-FFE5EF870D7BA81A -m 00000000000000000 download
</em> and let it get downloaded.
 <h3>2.Creating a bootable pendrive:</h3>
On windows, proceed with rufus directly and create a boot-able drive with fat32 file type, Bios or Uefi, and a gpt partition scheme and eh voila you've got your boot-able drive. Transfer the basesystem from x64 page and add it inside a folder named <em>com.apple.recovery.boot</em> in your USB drive. Now proceed to transfer the borrowed efi and place it inside the main directory of your USB drive.
<h3>3.Installation</h3>
Installing it is quite simple, boot off it, wipe the disk in APFS file system in the utilities tab up there. Install it into the drive you've wiped off. It should restart on its own and you might have to do the whole process again or installing it, once that happens, boot into your hackintosh and voila you've scammed the system my mate.
<em><h3><strong> For further info/ more deets into the technical aspect of it, read through the <a href="https://dortania.github.io/OpenCore-Install-Guide/">Opencore mannual</a></strong></h3></em>
# Configuration
	CPU: i5 8300H<br />
	iGPU: Intel UHD Graphics 630<br />
	dGPU: GeForce GTX 1050Ti<br />
	Chipset: Coffee Lake<br />
	Touchpad: Elan I2C HID<br />
	Keyboard: PS/2 <br />
	Audio: <br />
	Network: <br />
		-Wifi+BT: Intel Wireless-AC 9560<br />
		-Ethernet: Realtek PCIe GbE family Controller<br />
	Drives:<br />
		HDD: Western Digital WD10SPZX-21Z10T0 - 1TB(SATA)<br />
		SSD: SK hynix HFM256GDJTNG-8310A 256GB(NVMe)<br />
