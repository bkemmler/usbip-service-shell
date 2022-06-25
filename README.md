# usbip-service-shell

**usbip-service-shell** is a set of Linux services for the **USB/IP Project** that allows you to take no actions needed for handling sudden reboots and/or plug/unplug USB devices on fly


## Requirements, Conventions, Hardware or Software Version Used ##

Host - a Raspberry Pi 3B+ single board computer with  Rasbery OS
Client - ...

Installed on both machines:
 * OpenSSH_8.2p1
 * OpenSSL 1.1.1f 31 Mar 2020
 * usbip-utils 2.0
 * [Passwordless](https://www.redhat.com/sysadmin/passwordless-ssh) SSH Login for the other root.

 * apt install usbip

## Instructions
 - copy files [here](https://github.com/alpertsev/usbip-service-shell/tree/main/host) to your Host Computer and files [here](https://github.com/alpertsev/usbip-service-shell/tree/main/client) to your Client Computer as file structures dictate.
 - on both machines change IP-addresses of your host / client in client/host's **/root/.ssh/config** files and run **sudo systemctl enable usbipd && sudo systemctl start usbipd**
 - run **sudo systemctl enable usbipd-restart** on your Client Computer
 - enjoy!

## Known Issues
- silenced canberra-gtk-play

## Development
 - v0.1.0 initial release.
 - v0.1.1 faster ssh-command execution and no config files in use.
 - ~~Power Management implementation for USBIP Host~~
 - ~~make BT version, additionally to Wi-Fi~~
 - ~~Proximity Sensor Interface to wake up the host~~
 
## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## Acknowledgment
- [Takahiro Hirofuchi](http://usbip.sourceforge.net/) - A famous USB-IP implementation proven by years!!
- [Alexey Pertsev](https://www.alpertsev.com/) - usbip-service-shell-v0.1.0 developer - [Donate](https://paypal.me/alpertsev)

## License
[Apache-2.0](http://www.apache.org/licenses/LICENSE-2.0)
