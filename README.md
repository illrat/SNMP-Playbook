# SNMP Playbook

This Ansible playbook automates the deployment and configuration of SNMP (Simple Network Management Protocol) on Debian and RedHat based systems.

## Features

- Supports Debian and RedHat based distributions
- Automates SNMP installation and configuration
- Configures basic SNMP settings

## Prerequisites

- Ansible (version 2.9 or later recommended)
- SSH access to target machines
- Sudo privileges on target machines

## Usage

1. Clone this repository:
   ```
   git clone https://github.com/illrat/SNMP-Playbook.git
   cd SNMP-Playbook
   ```

2. Update the `hosts` file with your target hosts:
   ```
   [hosts]
   192.168.1.100
   192.168.1.101
   ```

3. Modify the `default/main.yaml` file to set your desired SNMP community string and other configurations.

4. Run the playbook:
   ```
   ansible-playbook -i inventory snmp_playbook.yml
   ```

## Configuration

You can customize the SNMP configuration by modifying the variables in `group_vars/all.yml`:

- `snmp_community`: Set your desired SNMP community string (default: "public")
- `snmp_location`: Set the physical location of the device
- `snmp_contact`: Set the contact information for the device administrator

## Supported Platforms

- Debian/Ubuntu
- RedHat/CentOS

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.


## Disclaimer

This playbook is provided as-is. Always test in a non-production environment before using in production.

## Support

For issues, questions, or contributions, please open an issue in the GitHub repository.
