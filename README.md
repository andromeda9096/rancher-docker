## Rancher single host with docker
https://rancher.com/docs/rancher/v2.x/en/installation/other-installation-methods/single-node-docker/

### Install Rancher using docker
- Change your port on host
- Version images

```
docker run -d --restart=unless-stopped -p 8181:80 -p 8443:443 --privileged rancher/rancher:v2.6-head
```

- Findout your default password login Rancher
```
docker logs  <containerID>  2>&1 | grep "Bootstrap Password:"
```

### Login Web UI

https://ip_host:8443

#### note:rancher need a domain with tls for k8s connect to



