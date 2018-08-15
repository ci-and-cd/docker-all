# docker-all

All docker modules managed by git submodule

Created by
```bash
find . -name '.git' | grep docker- | grep -v docker-all | awk -F/ '{print $2}' | sort | xargs -i echo git submodule add git@github.com:ci-and-cd/{}.git {}
```


## Access host from/inside containers (Docker for Mac)

see: https://forums.docker.com/t/access-host-not-vm-from-inside-container/11747/38

a) Loopback device in System Preferences visible
$ sudo networksetup -createnetworkservice Loopback lo0

b) setup the ip
$ sudo networksetup -setmanual Loopback 172.16.123.1 255.255.255.0

docker.for.mac.localhost is a special DNS name that resolves to the host IP
