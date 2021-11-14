Alternative ways to install RetroArch that I've tried, but don't keep up with.

The best way to install RetroArch, I think is PiKISS.  More details here:

https://github.com/LowTechCoder/rpi4-retroarch-guide/blob/main/README.md

### Method 1: Snap
The first way I ever installed RetroArch was to install a Snap.  This is by far the easiest way, but I believe it updated it's self one day without asking me and broke it's self.  So, if you do use this method and it works, you'll need a way to disable auto updates, which I will provide below.

Use a Terminal to install snapd and retroarch:
```
sudo apt install snapd -y
```
Reboot the Raspberry Pi 4

Now lets install RetroArch
```
sudo snap install retroarch
```
Disable Snapd from auto updating.  This is new to me, and I hope it holds up forever, but we'll see, and I'll update this guide if it ever fails me.
```
sudo systemctl mask snapd.service
```
If you ever do want to udpate a Snap you'll need to do this: (I haven't tested this yet.)
```
sudo systemctl unmask snapd.service
snap refresh
```

### Method 2: Compile RetroArch
An alternative way to install RetroArch is to Compile it from source.  I found a great tutorial on how to do that here:
https://gist.github.com/ematysek/fc01a47c7d34f0ca4dad41226c53ff6e

### Method 3: FlatPak
Another way you could install RetroArch is a FlatPak.  I have tried this method, and it works, but it's extremely slow to install and seems to install a ton of things probably not needed.  You can explore this method your self.  If it seems to get better over time, I'll update this guide and show some examples.
