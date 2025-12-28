
# Create new rules file

1. Using your preferred text editor create a new file and paste in the following content:

```
# ROG Falcata
SUBSYSTEM=="hidraw", ATTRS{idVendor}=="0b05", TAG+="uaccess"
SUBSYSTEM=="usb", ATTRS{idVendor}=="0b05", TAG+="uaccess"
```

Save as `70-asus.rules` .

2. Move the file to /etc/udev/rules.d/

	`sudo mv /path/to/saved/70-asus.rules /etc/udev/rules.d/`

Then run: 

	sudo udevadm control --reload-rules && sudo udevadm trigger

Or reboot your system. 

3. Open the [Gear Link](https://gearlink.asus.com/en) website using a [Chromium based browser.](https://en.wikipedia.org/wiki/Chromium_(web_browser)#Browsers_based_on_Chromium)

	- Click `Connect`.
	- On the pop up window choose `ASUSTek Computer, Inc. ROG SPEEDNOVA 8K RECEIVER` then click `Connect`. 

# Attribution
Thank you to `Adam Algaert` from The Full Nerd linux discord channel for pointing me in the right direction for this fix. 