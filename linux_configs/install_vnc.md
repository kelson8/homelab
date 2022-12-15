# The steps I used to install vnc:

I use xfce for vnc since it's lightweight, and tightvnc for the server it works well for me.

1. sudo apt update 
2. sudo apt install xfce4 xfce4-goodies tightvncserver
3. Move the file from linux_configs/systemd/vncserver.service to /etc/systemd/system/
4. For ssh forwarding add "AllowTcpForwarding yes" and "X11Forwarding yes" to /etc/ssh/sshd_config

Optional:\
 Set vncserver to auto start on boot: sudo systemctl enable --now vncserver.service
