- #ollama #mox
	- **Cấu hình của LXC ollama**
	  arch: amd64
	  cores: 4
	  features: nesting=1
	  hostname: ollama
	  memory: 12288
	  net0: name=eth0,bridge=vmbr0,firewall=1,hwaddr=BC:24:11:6F:82:55,ip=dhcp,type=veth
	  ostype: debian
	  rootfs: local-lvm:vm-100-disk-0,size=30G
	  swap: 4096
	  unprivileged: 1
	  lxc.cgroup2.devices.allow: c 10:200 rwm
	  lxc.mount.entry: /dev/net/tun dev/net/tun none bind,create=file
	- Trong LXC Ollama có cài [**langfuse**](https://langfuse.com/self-hosting/deployment/docker-compose), chạy bằng **docker** #langfuse #goose
		-
	-
	- **ollama login**: root-47
-