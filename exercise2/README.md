# Static IP Configuration Project

### Description
This project is designed to set static IP addresses for virtual machines running in a Hyper-V environment using an Ansible Playbook. It utilizes an external YAML file to define IP and gateway parameters for each machine, allowing configuration changes without modifying the playbook code itself.

---

### Table of Contents
- [Static IP Configuration Project](#static-ip-configuration-project)
    - [Description](#description)
    - [Table of Contents](#table-of-contents)
    - [Project Content](#project-content)
    - [Project Structure](#project-structure)
    - [Execution](#execution)
    - [Playbook Content](#playbook-content)
    - [Troubleshooting](#troubleshooting)

---

### Project Content

- **inventory.ini**: Inventory file containing information about the target machines.
- **static-ip.yaml**: Ansible Playbook file that configures the static IP address on each machine.
- **ip_allocation.yaml**: External YAML file specifying IP addresses and gateways for each machine.

---

### Project Structure


---

### Execution

1. **Edit IP Addresses**: Modify the `ip_allocation.yaml` file to set the IP addresses and gateways for each machine.
2. **Run the Playbook**: Run the following command from the main controller machine:

    ```bash
    ansible-playbook -i inventory.ini static-ip.yaml
    ```

---

### Playbook Content

`static-ip.yaml` includes the following tasks:

- **Set Static IP and Gateway**: Uses the `nmcli` module to configure the static IP and gateway as defined in the `ip_allocation.yaml` file.

---

### Troubleshooting

1. **Duplicate IP Addresses**: If all machines receive the same IP address, check that the `ip_allocation.yaml` file contains unique IP addresses for each target machine.

2. **Playbook Run Issues**: If the playbook fails to execute, verify that the `inventory.ini` file has correct target addresses and that SSH connectivity is established.

3. **IP Address Not Updating**: If the static IP address does not update after the playbook runs, try rebooting the virtual machine to apply the new settings.

---

Good luck!
