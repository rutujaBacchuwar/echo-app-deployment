# Echo App Deployment
Development Environment for echo-app provisioning and reverse proxy configuration.

# Prerequisites
1. Oracle Virtualbox
1. Vagrant
1. Ansible

# Setup Instruction
1. Clone this repository: `git clone <repo-url>`
1. Change to the application directory: `cd echo-app`
1. Install ansible roles: `ansible-galaxy install -r roles.yml -p roles`
1. Start VMs and configure: `vagrant up`
