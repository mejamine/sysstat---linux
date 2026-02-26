# Sysstat Installation and Configuration

This repository includes a playbook that installs and configures **sysstat** on Linux systems (Debian and RedHat families).  

It ensures the package is installed, enabled, configured, and properly collecting performance statistics.

---

## Tasks:

- Install **sysstat** package if not present  
- Enable and start sysstat service  
- Configure sysstat (Debian only)  
- Create systemd override for **sysstat-collect.timer**  
- Configure collection interval using `sysstat_interval`  
- Restart sysstat timer if configuration changes  

---

## Supported Operating Systems

- Debian / Ubuntu  
- RedHat / Fedora 

---

## Using in AAP

### General Config :
1. **Inventory:** create from file or manually  
2. **Credential:** SSH username/password + sudo  

This playbook **requires a survey variable** for the collection interval (`sysstat_interval`) rather than hardcoding it in the playbook.  

---

## Variables

### Playbook Variables (already defined inside the playbook)

- `sysstat_config_file_debian` → `/etc/default/sysstat`  


### Hosts variables : (in hosts.ini or create manually in AAP) (inventory related)

- `ansible_host` – ip address of the host  
- `ansible_user` – username of the host user  
- `ansible_os_family` – OS family (Debian / RedHat)  



