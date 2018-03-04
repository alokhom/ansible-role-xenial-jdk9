# README.md
# Ansible Role: ansible-role-xenial-jdk9

An Ansible role that installs ansible-role-xenial-jdk9 on xenial

## Requirements
- Python 2.7 installed on any xenial machine.
- Ansible 2.4 installed on any controller machine.
- Downloads the openjdk9 deb for the first time in the target machine and keepts if for future. You can change your java deb url accordingly as and when you want to...
- Automatically Sets JAVA environment to java_home: "/usr/lib/jvm/java-9-openjdk-amd64"

## Role Variables

Available variables are listed below, along with default values:

  - reconfigure the target_user variable to be your target machine remote user.
  - Automatically Sets JAVA environment to java_home: "/usr/lib/jvm/java-9-openjdk-amd64"

## Dependencies

- it is tested well on xenial64 vagrant and also is ok for other xenial docker images and servers. 
- it is expected to work fine for linux machines.

## Example Playbook

    - hosts: xenialhostip
      roles:
        - role: alokhom.j
          when: "ansible_os_family == 'Debian'"

## License

MIT

