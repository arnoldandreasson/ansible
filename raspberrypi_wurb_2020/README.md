# Ansible for CloudedBats WURB 2020

## Notes (should be part of instruction)

Ansible playbook...

Raspberry Pi Imager
Raspberry Pi OS Lite (32-bit)

"Gearwheel"

Hostname: wurb99
Enable SSH
Use password authentication
Username: pi
Password: my-wurb99-password
Configure wireless LAN
- SSID: my-home-wifi
- Password: my-home-wifi-password
- Wireless LAN country: SE
Locale settings
- Time zone: Europe/Stockholm
- Keyboard layout: se

ssh-copy-id pi@wurb99.local

ansible -i inventory.yaml wurbs -a "df -h"

ansible-lint playbook.yaml

ansible-playbook -i inventory.yaml -v playbook.yaml --check

ansible-playbook -i inventory.yaml -v playbook.yaml --limit "wurb99"
