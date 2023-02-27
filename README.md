# USB forwarding(USB IP)


### On the server side(laptop):

```sudo apt-get install linux-tools-generic```

```sudo modprobe usbip_host```

```sudo nano /etc/modules```

add ```usbip_host``` to the end of texts

```lsusb``` to see a list of attached USB devices

```sudo usbip list -p -l```

```sudo usbip bind --busid=``` enter busid from the above list command

```sudo usbipd```

### On the client side(rpi):

```wget http://raspbian.mirror.net.in/raspbian/raspbian/pool/main/l/linux/usbip_2.0+5.10.158-2+rpi1_armhf.deb```

```sudo modprobe vhci-hcd```

```sudo nano /etc/modules```

add ```vhci-hcd``` to the end of texts

```sudo usbip attach -r ipa-b busid```

