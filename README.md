# Sysstat Installation and Configuration (Debian Family)

This repository includes a playbook that installs and configures **sysstat** on Linux systems.

The playbook ensures that the `sysstat` package is installed, properly enabled (for Debian-based systems), and that the service is started.

---

## Tasks:

- Install `sysstat` package if not present  
- Configure sysstat for Debian family systems  
- Enable and start `sysstat` service  

---

## Supported Operating Systems

### Supported:
- Debian  
- Ubuntu  
- Other Debian-based distributions  

⚠️ The configuration step (`ENABLED="true"`) is applied only on Debian family systems.

---

## Using in AAP

### General Config :

1. **Inventory:** create from file or manually  
2. **Credential:** SSH username/password + sudo  

No survey is required for this playbook.

---

## Variables

### Playbook Variables (defined inside the playbook)

```yaml
sysstat_config_file_debian: /etc/default/sysstat