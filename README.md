# Go Relayer Ansible Deployment

## Design Philosophy

1. Support rly only
1. Make config file composable and extensible with DRY principle

## Guide

First copy it to your own inventory file so you can customize it to suit your needs:

```bash
cp inventory.sample inventory
```

### rly Installation

```bash
ansible-playbook install.yml
```

### rly deployment

You will need to specify `key_name`, `memo` and a list of target ips in the inventory file. Examples are provided in the sample file.

```bash
ansible-playbook main.yml -e "target=mainnet"
ansible-playbook main.yml -e "target=testnet"
```
