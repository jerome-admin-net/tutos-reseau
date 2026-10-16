# 🧪 Lab 01 : Configuration de VLANs sur Switch Cisco

## 1. Objectif du Lab
Mettre en place deux VLANs séparés (**VLAN 10 COMPTA** et **VLAN 20 PROD**) sur un switch Cisco afin de segmenter le trafic réseau.

---

## 2. Configuration étape par étape

### Étape 1 : Création des VLANs
```bash
enable
configure terminal
vlan 10
 name COMPTA
vlan 20
 name PROD
exit

interface FastEthernet 0/1
 switchport mode access
 switchport access vlan 10
exit

show vlan brief
