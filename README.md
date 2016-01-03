This repo hosts Ansible playbooks to configure a Centos 7 machine for Continuous Integration and Delivery.

The setup is splitted in different modules

- Security
  - Hardening of SSHD and configuration of users
- Java
  - Installation of JDK (currently 8)
- Teamcity
  - Installation of Teamcity CI server
- Nexus
  - Installation of Nexus artifact repository
- Sonar
  - Installation of SonarQube code analysis tool

To trigger the installation one must run

`ansible-playbook -i inventory_new_machines.yml playbook_prepare_new_machine.yml --ask-vault-pass`

Note to self: remember to install gradle.properties with deployment passwords in ~/.gradle directory (and crypt it with ansible-vault)
