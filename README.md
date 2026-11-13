# L3-L4-Firewalls
# Perimeter Firewall Lab: Three-Zone Security Architecture

## Overview
This repository implements a three-zone network topology (LAN, DMZ, and WAN) using Containerlab and an Alpine Linux perimeter router configured with `iptables`. The firewall enforces stateful packet inspection, blocks a blacklisted external threat actor, isolates the internal LAN from unsolicited external traffic, and restricts WAN access to the DMZ web server strictly to HTTP (`80/tcp`) and HTTPS (`443/tcp`).

## Directory Layout
* `lab.clab.yml` — Containerlab topology, IP addressing, routing, and link definitions.
* `config/iptables.rules` — Firewall filtering policy loaded onto the perimeter router.
* `README.md` — Lab documentation and deployment instructions.

## Deployment
Deploy the topology and apply all network and firewall configurations:
```bash
sudo clab deploy -t lab.clab.yml
