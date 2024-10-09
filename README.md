# Ansible Project

This repository contains an Ansible project for managing common packages and ZeroTier network configurations on various Linux distributions.

## Directory Structure

```
.
├── ansible.cfg             # Ansible configuration file
├── deploy.yml              # Playbook for deploying packages
├── group_vars              # Directory containing group variable files
│   ├── all
│   │   └── vars            # Variables for all hosts
│   ├── development         # Variables specific to development environment
│   └── productions         # Variables specific to production environment
├── host_vars               # Directory containing host variable files
│   └── hostnames
│       └── vars            # Variables specific to hosts
├── inventory               # Inventory file for defining hosts and groups
│   └── hosts.ini           # Hosts and groups definition
├── README.md               # Project documentation
├── roles                   # Directory for roles
│   ├── common_package      # Role for managing common packages
│   │   ├── defaults        # Default variables for common_package role
│   │   │   └── main.yml    # Default variables file
│   │   └── tasks           # Directory for tasks related to common_package role
│   │       ├── deploy.yml   # Tasks for deploying common packages
│   │       ├── main.yml     # Main tasks file for common_package
│   │       └── undeploy.yml # Tasks for undeploying common packages
│   └── net.zerotier       # Role for managing ZeroTier network configuration
│       ├── defaults        # Default variables for net.zerotier role
│       │   └── main.yml    # Default variables file
│       └── tasks           # Directory for tasks related to net.zerotier role
│           └── main.yml    # Tasks for managing ZeroTier network
└── undeploy.yml            # Playbook for undeploying packages
```

## Requirements

- Ansible 2.9 or higher
- Supported Linux distributions: Ubuntu, Debian, AlmaLinux

## Usage

1. **Deploy Packages**
   To deploy common packages, run the following command:
   ```
   ansible-playbook deploy.yml
   ```

2. **Undeploy Packages**
   To remove common packages, run the following command:
   ```
   ansible-playbook undeploy.yml
   ```

## Roles

- **common_package**: Manages installation and removal of common packages across different distributions.
- **net.zerotier**: Configures and manages ZeroTier network settings.

## Contribution

Feel free to submit issues or pull requests for improvements or fixes.
