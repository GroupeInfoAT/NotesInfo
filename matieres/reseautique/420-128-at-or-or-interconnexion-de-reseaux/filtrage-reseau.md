---
description: Règles de pare-feu et listes de contrôle d'accès
---

# Filtrage réseau

Pare-feu

* Le WAN est composé d'inconnus
* Stranger danger
* Prévient la propagation d'un danger
* Délimiter des zones réseau (Réseau étendu : Généralement Internet, réseau sur lequel nous n'ont pas de contrôle.../ Intranet: Réseau local.../ Publique : Réseau mis à la disposition des visiteurs donnant généralement accès à Internet et à certains équipements mis à la disposition des visiteurs (imprimantes)/ Démilitarisée (DMZ): Zone à sécurité accrue hébergeant les services et serveurs accessibles depuis le réseau étendu)
* DST-NAT
* Filtrer le trafic entre les zones

NGFW: Next-Generation Firewall

* Inspection
* Journalisation
* Protection

Actions

* Accepter -> ..
* Bloquer -> Intercepter ..
* Abandonner -> Ignorer le trafic complètement, possible de journaliser (Si face au réseau attendu)



Conditions

* Source
* Destination
* Protocole
* Port
* Contenu\*

Pourquoi?

* Améliorer notre posture en sécurité
* Améliorer la résilience aux pannes de notre réseau
* Optimiser les performances de notre réseau

{Low Orbit lon cannon}





