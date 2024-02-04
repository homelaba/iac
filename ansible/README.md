# Ansible container for run commands 

simple ansible plays

## Build

```bash
docker build -t ansible .
```

## SSH settings

**public key**
is required for initial setup `/ssh/ids_rsa.pub`

**private key**
used for connection and configuration, instead of the standard password, so as not to configure ssh config by default `/ssh/ids_rsa`

## Settings environment

```bash
cp .example.env .env
```

Change variables

## Usage

Run + exec container
```bash
docker run --rm -it -v ${pwd}:/ansible --env-file .env ansible bash
```

Create LXC
```bash
ansible-playbook /ansible/lxc/lxc_create.yaml -i /ansible/hosts.yaml
```

Remove LXC
```bash
ansible-playbook /ansible/lxc/lxc_remove.yaml
```

or
```bash
docker run --rm -it -v ${pwd}:/ansible --env-file .env ansible /ansible/lxc/lxc_remove.yaml
```


