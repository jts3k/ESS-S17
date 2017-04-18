Download the Pi disk image [here](https://drive.google.com/file/d/0B5KAwRis5WlVSWwzNk1mYVY2UFk/view?usp=sharing).  Use [Pi Filler](http://ivanx.com/raspberrypi/) to copy this disk image onto an SD card.  This will give you a working machine that automagically boots up into a PureData patch called *launch.pd*.

To connect to your Pi from a Mac you'll need a ethernet adapter thing so you can connect via, you know, ethernet.  In System Preferences/Network set up your ethernet connection with a Manual IP address of 10.0.0.1 and a Subnet Mask of 255.255.0.0.

To view your Pi desktop from the Mac: open up Terminal and enter ```ssh pi@10.0.0.2```.  The pi password is ```3.14ispi```.  Once you're connected enter ```vncserver``` to start a virtual desktop on the Pi.  Back on your Mac do "Finder/Go/Connect to Server..." (Command K) and enter ```vnc://10.0.0.2:5901```.
