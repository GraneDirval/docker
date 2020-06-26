# docker-network-fix
> /etc/docker/daemon.json
```
{
  "default-address-pools":
  [
    {"base":"172.26.0.1/16","size":24}
  ]
}
```
`sudo systemctl restart docker`


To fix `cgroups: cannot found cgroup mount destination: unknown`

`sudo mkdir /sys/fs/cgroup/systemd`

`sudo mount -t cgroup -o none,name=systemd cgroup /sys/fs/cgroup/systemd`
