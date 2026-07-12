- #lxc
	- **lxcconfig để cài tailscale trên lxc**
		- vào file config của lxc băng shell của parent node
		  nano /etc/pmv/lxc/[idnumber.conf]
		- thêm 2 dòng sau vào file config và save lại
		  lxc.cgroup2.devices.allow: c 10:200 rwm
		  lxc.mount.entry: /dev/net/tun dev/net/tun none bind,create=file
		- chạy script sh cài đặt tailscale
		  curl -fsSL https://tailscale.com/install.sh | sh