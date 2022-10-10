# ansible-role-ubuntu-cloudinit

###### Status: Unstable

Configures an Ubuntu installation to be cloud-init aware and therefore be usable as a template OS image

## Example

```yaml
- name: Reenable cloud-init
  ansible.builtin.include_role: mangadex.ubuntu_cloudinit
  vars:
    # Optional, avoids wasting time with metadata discovery if you always use the same datasource
    cloud_init_single_source: NoCloud
    
    # Optional, allows overriding some cloud-init parameters; with this setup being a sensible default
    cloud_init_cfg_overrides:
      package_update: true
      package_upgrade: true
      package_reboot_if_required: true
```
