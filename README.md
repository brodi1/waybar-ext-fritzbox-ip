# waybar-ext-fritzbox-ip

...is a [waybar](https://github.com/Alexays/Waybar) module that allows you to see your current external ip without a third party api, instead it sends a request directly from your machine to your FritzBox.

### Requirements:
- a FritzBox
- [waybar](https://github.com/Alexays/Waybar) (including some basic skills how to edit the waybar config file)
- [sway](https://github.com/swaywm/sway)
- git
- wget
- grep

### Steps to install:

Skip the 1. step if you have already a modules folder

1. `mkdir -p ~/.config/waybar/modules/`
2. `git clone https://github.com/brodi1/waybar-ext-fritzbox-ip.git`
3. `cd waybar-ext-fritzbox-ip`
4. (Optional) change the IP address in the `fritz-ext-ip.sh` file if your local FritzBox IP **is not** 192.168.178.1
5. `cp -r fritz-ext-ip.sh ~/.config/waybar/modules/`
6. add this to your `~/.config/waybar/config` file:

```
"custom/fritz-ext-ip": {
	"format": "{}",
	"interval": 20,
	"exec": "~/.config/waybar/modules/fritz-ext-ip.sh"
	},
```

7. add `"custom/fritz-ext-ip"` to your [waybar](https://github.com/Alexays/Waybar) module list

8. (Optinal) add this to your file to change the styling:

   ```
   #custom-fritz-ext-ip {
           font-size: 10px;
   }
   ```

   

### To get it working:
Just restart [sway](https://github.com/swaywm/sway) by pressing ***$mod+shift+c***



### Tested on:
- Arch Linux
- FritzBox 7490 v7.12

### Should also work on:
- FreeBSD
- and other FritzBox Routers

