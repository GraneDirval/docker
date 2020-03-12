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
