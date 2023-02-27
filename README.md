# USB forwarding(USB IP)


### On the server side(laptop):

1. ```sudo apt-get install linux-tools-generic```

2. ```sudo modprobe usbip_host```

3. ```sudo nano /etc/modules```

4. add ```usbip_host``` to the end of texts

5. ```lsusb``` to see a list of attached USB devices

6. ```sudo usbip list -p -l```

7. ```sudo usbip bind --busid=``` enter busid from the above list command

8. ```sudo usbipd```

### On the client side(rpi):

1. ```wget http://raspbian.mirror.net.in/raspbian/raspbian/pool/main/l/linux/usbip_2.0+5.10.158-2+rpi1_armhf.deb```

2. ```sudo modprobe vhci-hcd```

3. ```sudo nano /etc/modules```

4. add ```vhci-hcd``` to the end of texts

5. ```sudo usbip attach -r ip -b busid```

