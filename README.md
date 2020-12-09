My configurations for slstatus

Usage
--------
slstatus might be the easiest tool developed by the suckless community. All the the features are commented inside the `config.h` header file. slstatus also allows custom scripts. 

```bash
git clone https://github.com/manu-febie/slstatus.git
```

```bash
sudo make clean install
```

I don't use any display manager so I add `slstatus` inside my `.xinitrc` file. Always make sure you `exec dwm` at the end of the file.

```bash
# xinitrc
exec slstatus &
```

Example configurations
--------
```c 
/* config.h */
static const struct arg args[] = {
	/* function format          argument */
	{ keymap,    " keyb %s ",      NULL			  },
	{ wifi_perc, " wifi %s%% ",    "wlp2s0"       },
	{ cpu_freq,  " cpu %s ",       NULL           },
	{ ram_used,  " mem %s",        NULL           },
	{ separator, "/",              NULL           },
	{ ram_free,  "%s ",             NULL           },
	{ datetime,  " %s ",           "%b %d %Y, %R" },
};
```


Features
--------
- Battery percentage/state/time left
- CPU usage
- CPU frequency
- Custom shell commands
- Date and time
- Disk status (free storage, percentage, total storage and used storage)
- Available entropy
- Username/GID/UID
- Hostname
- IP address (IPv4 and IPv6)
- Kernel version
- Keyboard indicators
- Keymap
- Load average
- Network speeds (RX and TX)
- Number of files in a directory (hint: Maildir)
- Memory status (free memory, percentage, total memory and used memory)
- Swap status (free swap, percentage, total swap and used swap)
- Temperature
- Uptime
- Volume percentage
- WiFi signal percentage and ESSID


