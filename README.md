# ansible-role-linux-hardening

Ansible role for Linux baseline hardening: SSH, nftables, PAM, sysctl, services, updates, auditd, login banners and fail2ban.

Extracted from [ansible-linux-hardening](https://github.com/0xseb000/ansible-linux-hardening) so it can be consumed as a versioned dependency. That repository remains the original submission and its lab setup; this one contains the role only.

Used by [ansible-detection-lab](https://github.com/0xseb000/ansible-detection-lab).

## Usage

```yaml
# requirements.yml
roles:
  - name: hardening
    src: https://github.com/0xseb000/ansible-role-linux-hardening
    version: v1.0.0
```

```yaml
- hosts: targets
  become: true
  roles:
    - hardening
```

## Requirements

Ubuntu 24.04, Ansible 2.15+

## Variables

See `defaults/main.yml`.
