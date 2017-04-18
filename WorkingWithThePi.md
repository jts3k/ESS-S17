Download the Pi disk image [here](https://drive.google.com/file/d/0B5KAwRis5WlVSWwzNk1mYVY2UFk/view?usp=sharing).  Use [Pi Filler](http://ivanx.com/raspberrypi/) to copy this disk image onto an SD card.  This will give you a working machine that automagically boots up into a PureData patch called *launch.pd*.

To connect to your Pi from a Mac you'll need a ethernet adapter thing so you can connect via, you know, ethernet.  In System Preferences/Network set up your ethernet connection with a Manual IP address of 10.0.0.1 and a Subnet Mask of 255.255.0.0.

To view your Pi desktop from the Mac: open up Terminal and enter ```ssh pi@10.0.0.3```.  If you're connecting for the first time you'll be asked if you trust this computer (you do).  The pi password is ```3.14ispi```.  If PD is running on the Pi you'll see a repeating message "signalling PD..." - you can kill this be entering Control-C.

Once you're connected to the Pi enter ```vncserver``` to start a virtual desktop on the Pi.  Back on your Mac do "Finder/Go/Connect to Server..." (Command K) and enter ```vnc://10.0.0.3:5901```.

You'll probably want to edit the PD patches on a "real" desktop, so copy the PD files from the Pi to your laptop for editing then copy them back when you're ready to test them on the Pi.

To copy all the PD files from the Pi to your Mac enter this in the terminal: ```scp -r pi@10.0.0.3:Documents/PD /Users/YourUserName/Documents/PD```

To copy files from the Mac to the Pi in mac terminal: ```scp -r /Users/YourUserName/Documents/PD pi@10.0.0.3:Documents/PD```
