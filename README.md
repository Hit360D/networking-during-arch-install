# networking-during-arch-install

This is to be done while being chrooted into the mounted disk as root.

## Set the Hostname file

The following creates a hostname file and adds your hostname to it.

```echo [your_hostname] > /etc/hostname```

## Create a hosts file

```touch /etc/hosts```

Add the following content to the new hosts file. You can use your prefered editor.

127.0.0.1 localhost\ ::1 localhost\ 127.0.1.1 [your-hostname]

## Enable Dynamic Host Configuration Protocol (DHCP)

```systemctl enable dhcpcd```

If you don't have dhcpcd, you can install it using pacman.
