# Infrastructure as code (IaC)

## Experiments on homelab management

General infrastructure and scheme (excalidraw image)

![scheme](./.images/scheme.excalidraw.png)

Base image for gitlab ci https://github.com/akmalovaa/iac-tools

### LXC

> LXC  is the minimum unit in my home laboratory (equivalent pod in k8s)

LXC - A Proxmox container is a type of virtualization that allows you to run applications within isolated environments on a Proxmox Virtual Environment (PVE) host. LXC Proxmox containers share the host system’s kernel but maintain their separate user space, making them lightweight. They’re great for deploying applications with less total overhead than virtual machines, which allows for more efficient resource usage.

- Easy to create, delete, backup
- Auto transfer to live node in Proxmox Cluster
- Another layer of security
- Easier to maintain (if something breaks, it will be inside only this application)

### Ansible

for create LXC, install soft, infrastructure preparation
Gitlab is used for deployment

## Services

#### Proxy server

[Traefik](https://github.com/traefik/traefik) 

Alternatives:
- [caddy](https://github.com/caddyserver/caddy)
- [nginx proxy manager](https://github.com/NginxProxyManager/nginx-proxy-manager)

#### DNS

[blocky](https://github.com/0xERR0R/blocky)

Alternatives:
- [AdGuardHome](https://github.com/AdguardTeam/AdGuardHome)
- [pi-hole](https://github.com/pi-hole/pi-hole)