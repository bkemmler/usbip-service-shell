# usbip-service-shell

**usbip-service-shell** is a set of Linux services for the **USB/IP Project** that allows you to take no actions needed for handling sudden reboots and/or plug/unplug USB devices on fly

## Requirements, Conventions, Hardware or Software Version Used ##

Host - a Raspberry Pi 4 single board computer with  Rasbery OS
Client - ...

Installed on both machines:
 * apt install usbip


## Instructions HOST
 - copy & modify files if need https://github.com/bkemmler/usbip-service-shell/tree/main/host/etc to your Host Computer 
 - systemctl daemon-reload
 - systemctl enable usbipd
 - sudo systemctl start usbipd

## Instructions Client
 - mkdir /opt/usbip
 - mkdir /var/spool/usbip
 - copy & modify files if need https://github.com/bkemmler/usbip-service-shell/tree/main/client to your Client Computer
 - sudo chmod +x /opt/usbip/usbip-attach 
 - systemctl daemon-reload
 - systemctl enable usbip-attach
 - systemctl start usbip-attach
 
## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## Acknowledgment
- https://github.com/alpertsev/usbip-service-shell
- https://unix.stackexchange.com/questions/406847/use-usbip-for-devices-that-are-being-removed-and-reconnected

## License
[Apache-2.0](http://www.apache.org/licenses/LICENSE-2.0)
