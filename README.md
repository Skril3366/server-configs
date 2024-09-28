# server-configs

## Playbooks

To set everything up run

```bash
ansible-galaxy install -r requirements.yaml
```

### users.yaml

> This playbook creates `appuser` which is used to run applications. Also it
> setups the same ssh keys as for the root.

Running playbooks:

```bash
ansible-playbook -i hosts.yaml playbooks/users.yaml
```

### tailscale.yaml

> This playbook installs tailscale and sets it up as exit node. For that you
> must set tailscale_authkey in tailscale.yaml. You can obtain it at
> https://login.tailscale.com/admin/settings/keys

```bash
ansible-playbook -i hosts.yaml playbooks/tailscale.yaml
```
