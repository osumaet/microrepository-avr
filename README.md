# MICROREPOSITORY-AVR
Set of projects for AVR. Each project completly independend from others.

Content notes
------------
* If you do not use VSCode, you will remove `.vscode` folder. It's ok.
* Check `PORT` in Makefile for your particular device connection.

If you never compiled any avr c program (Linux instruction)
------------
Install all required sofware:

	sudo apt install make avr-gcc avr-libc binutils-avr avrdude

Device connection
------------
By default Linux users have no write or read access to USB-devices. Include your account in group `dialout`.

	sudo adduser my_user_login dialout

Also you can write custom udev rules for your devices.
