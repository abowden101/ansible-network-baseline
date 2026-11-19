# Ansible Network Baseline

Practical Ansible roles and playbooks for network automation.

Focused on:
- Configuration backup
- Golden config / baseline enforcement
- Simple compliance checks
- Multi-device inventory patterns

Built as a hands-on learning and portfolio project while transitioning into a Network Automation Engineer role.

---

## Quick Start (Cisco DevNet Sandbox)

```bash
# Install collections
ansible-galaxy collection install -r requirements.yml

# Run a backup against the free Cisco sandbox
ansible-playbook playbooks/backup.yml
```

---

## Structure

```
ansible-network-baseline/
├── inventory/
│   └── hosts.yml              # Example inventory (DevNet sandbox included)
├── group_vars/
│   └── all.yml                # Shared variables
├── roles/
│   └── network_baseline/      # Reusable baseline role
├── playbooks/
│   ├── backup.yml             # Config backup
│   ├── push_baseline.yml      # Push golden config pieces
│   └── compliance_check.yml   # Basic compliance checks
├── ansible.cfg
└── requirements.yml
```

---

## Playbooks

| Playbook | Purpose |
|----------|---------|
| `playbooks/backup.yml` | Backup running-config from devices |
| `playbooks/push_baseline.yml` | Apply login banner + NTP servers |
| `playbooks/compliance_check.yml` | Check for required settings |

---

## Roadmap

- [x] Config backup
- [x] Basic golden config push (banner + NTP)
- [x] Simple compliance checks
- [ ] Full golden config templates
- [ ] NetBox dynamic inventory
- [ ] Fortinet / multi-vendor support
- [ ] Ansible Automation Platform / AWX example

---

## Author

Antonio Bowden  
Network Engineer | Orlando, FL  
[GitHub](https://github.com/abowden101) · [Portfolio](https://abowden101.github.io/antonio-bowden-portfolio/)
