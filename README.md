# driller
A tool to install an network interface into a docker container. It also connects the interface with an existing host bridge.

# Required commands
- ip
- brctl
- iptables

# How to use

## Launch a Docker container
```
docker run --network none --name my_container debian
```


## Run ch a Docker container


The following example installs an netork interface in the container whose
ID is `my_container` with the IP address `192.168.1.50/24`. The interfaces is
connected to the host bridge `br0`.

```
sudo ./drill -a 192.168.1.50/24 -g 192.168.1.254 -b br0 my_container
```

# TODO
- remove iptables setting.
